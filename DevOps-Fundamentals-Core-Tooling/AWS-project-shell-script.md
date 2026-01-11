```
#!/bin/bash

set -x      # it will show the commands which we are running

This script will report the AWS resource usage

# AWS S3, AWS EC2, AWS Lambda, AWS IAM Users

# list s3 buckets
echo "Print list of s3 buckets"
aws s3 ls

# list ec2 instances
echo "Print list of ec2 instance"
aws ec2 describe-instances | jq '.Reservations[].Instances[].InstanceId'
aws ec2 desribe-instances

# list lambda
echo "Print lamdda"
aws lambda list-functions

# list iam users
echo "Print iam users"
aws iam list-users


```

**jq**

- JQ is a JSON parser used in Linux to read and extract specific information from JSON data (24:59). In the context of the video, it's used to simplify large outputs from AWS CLI commands by only showing the relevant details, such as an EC2 instance ID, rather than the entire JSON response (24:30-25:47).
- It's highlighted as a tool useful for DevOps engineers who often deal with JSON and YAML formats (24:54-24:58).


<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/46a54140-4399-4df4-8017-ccb3717cd621" />

```
aws ec2 describe-instances | jq '.Reservations[].Instances[].InstanceId'
```
<img width="1901" height="208" alt="image" src="https://github.com/user-attachments/assets/7079b1a4-b637-47be-90be-c4fc198e71a0" />

- What does [] mean?

[] means “iterate over a list (array)”

Good question — this is a **core concept** in JSON, `jq`, and AWS CLI queries.

---

## What does `[]` mean?

**`[]` means “iterate over a list (array)”**

In simple words:

> **“Take each item inside this list one by one.”**

---

## Example in JSON

```json
{
  "Fruits": ["apple", "banana", "mango"]
}
```

### Accessing the list:

```jq
.Fruits
```

Output:

```json
["apple", "banana", "mango"]
```

### Using `[]`

```jq
.Fruits[]
```

Output:

```text
"apple"
"banana"
"mango"
```

👉 `[]` **breaks the array into individual elements**

---

## In your AWS command

```bash
.Reservations[].Instances[].InstanceId
```

### Step-by-step:

### 1️⃣ `.Reservations[]`

* `Reservations` is a **list**
* `[]` → go through **each reservation**

### 2️⃣ `.Instances[]`

* Each reservation has an **Instances list**
* `[]` → go through **each instance**

### 3️⃣ `.InstanceId`

* Pick the `InstanceId` field from each instance

---

## Visual flow

```text
Reservations (array)
 ├─ Reservation 1
 │   └─ Instances (array)
 │       ├─ Instance A → InstanceId
 │       └─ Instance B → InstanceId
 └─ Reservation 2
     └─ Instances (array)
         └─ Instance C → InstanceId
```

---

## Very simple analogy 🧠

Think of `[]` like:

> **“For each item in the list”**

```text
For each Reservation
  For each Instance
    Print InstanceId
```

---

## Without `[]` vs With `[]`

❌ Without `[]` (wrong):

```jq
.Reservations.Instances.InstanceId
```

➡️ Fails because those are **arrays**

✅ With `[]` (correct):

```jq
.Reservations[].Instances[].InstanceId
```

---

## Key takeaway (remember this)

* `{}` → object (dictionary)
* `[]` → list (array)
* `[]` always means **loop through elements**

If you want, I can give you **2–3 quick practice questions** to lock this concept permanently 👍

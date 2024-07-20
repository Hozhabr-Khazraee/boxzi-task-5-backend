
# Following System API

## installation
Clone the project

```bash
python3 -m venv venv
source venv/bin/activate 
pip install -r requirements.txt
```

## adding test data

```bash
python3 add_test_data.py
```

## running server

```bash
export FLASK_APP=app.py
flask run
```

## using API

### listing users:
```bash
GET /users
```

### listing followers of a user:
```bash
GET /followers_count/<user_id>
```

### listing followers of two users:
```bash
GET /common_followers/<user1_id>/<user2_id>
```

### following:
```bash
POST /follow
Content-Type: application/json

{
    "follower_id": 1,
    "followee_id": 2
}
```

### unfollowing:
```bash
POST /unfollow
Content-Type: application/json

{
    "follower_id": 1,
    "followee_id": 2
}
```
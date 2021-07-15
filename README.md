# users table

| Column             | Type                | Options              |
|--------------------|---------------------|----------------------|
| email              | string              | null: false          |
| encrypted_password | string              | null: false          |
| name               | string              | null: false          |


# Association

has_many :items
has_one :buy

# items table

| Column             | Type                | Options              |
|--------------------|---------------------|----------------------|
| name               | string              | null:false           |
| category           | string              | null:false           |
| price              | integer             | null:false           |
| seller             | references          | foreign_key: true    |


# Association

belongs_to :user
belongs_to :buy

# buys table

| Column             | Type                | Options              | 
|--------------------|---------------------|----------------------|
| card_number        | integer             | null:false           |
| expiration_date    | integer             | null:false           |
| security_code      | integer             | null:false           |
| postal_code        | integer             | null:false           |
| prefectures        | string              | null:false           |
| municipality       | string              | null:false           |
| address            | integer             | null:false           |
| building_name      | string              |                      |
| phone_number       | integer             | null:false           |


# Association

has_many :items
belongs_to :user
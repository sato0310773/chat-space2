# Database

##users_table
|column        |type   |
|:-----        |----   |
|id            |       |
|name          |string |
|email         |string |
|password      |string |

###Association
+ has_many :group through :members
+ has_many :group_users
+ has_many :messages

##group_table
|column        |type   |
|:-----        |----   |
|id            |integer|
|name          |string |

###Association
+ has_many :users through :members
+ has_many :members
+ has_many :messages

##message_table
|column        |type   |
|:-----        |----   |
|text|         |text   |
|image|        |string |
|user_id|      |integer|
|group_id|     |integer|

###Asociation
+ belongs_to :user
+ belongs_to :group



##members_tables
|column        |type   |
|:-----        |----   |
|user_id|      |integer|
|group_id|     |integer|

###Asociation
+ belongs_to :user
+ belongs_to :group
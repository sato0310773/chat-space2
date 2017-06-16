# Database

##users_table
|column        |type   |
|:-----        |----   |
|name          |string |

###Association
+ has_many :group through :group_users
+ has_many :group_users
+ has_many :messages

##group_table
|column        |type   |
|:-----        |----   |
|name          |string |

###Association
+ has_many :users through :group_users
+ has_many :group_users
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



##group_users_tables
|column        |type   |
|:-----        |----   |
|user_id|      |integer|
|group_id|     |integer|

###Asociation
+ belongs_to :user
+ belongs_to :group
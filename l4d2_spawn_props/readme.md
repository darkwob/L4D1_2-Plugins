# Description | 內容
Let admins spawn any kind of objects and saved to cfg

* Work | 作品展示
    * [Unlimited Map C8 by Harry](https://www.youtube.com/watch?v=UTUjd6hlpt0)
    * [L4D2-Unlimited-Map](https://github.com/fbef0102/L4D2-Unlimited-Map)

* Image | 圖示
	* image 1
	<br/>![l4d2_spawn_props_1](image/l4d2_spawn_props_1.jpg)
	* image 2
	<br/>![l4d2_spawn_props_2](image/l4d2_spawn_props_2.jpg)
	* image 3
	<br/>![l4d2_spawn_props_3](image/l4d2_spawn_props_3.jpg)
	* image 4
	<br/>![l4d2_spawn_props_4](image/l4d2_spawn_props_4.jpg)
	* image 5
	<br/>![l4d2_spawn_props_5](image/l4d2_spawn_props_5.jpg)
	* image 6
	<br/>![l4d2_spawn_props_6](image/l4d2_spawn_props_6.jpg)
	* image 7
	<br/>![l4d2_spawn_props_7](image/l4d2_spawn_props_7.jpg)
	* image 8
	<br/>![l4d2_spawn_props_8](image/l4d2_spawn_props_8.jpg)
	* image 9
	<br/>![l4d2_spawn_props_9](image/l4d2_spawn_props_9.jpg)

* Apply to | 適用於
```
L4D1
L4D2
```

* Translation Support | 支援翻譯
```
English
繁體中文
简体中文
```

* <details><summary>Changelog | 版本日誌</summary>

	* v3.8 (2022-11-3)
        * Remake Code
        * Translation Support
        * some menu has back button
        * menu won't be disappeared if I spawn an object
        * Add more options
        * More objects
        * New Spawn Method: Items&Weapons, you can spawn Guns, Melees, Supplies, Throwables, etc.
        * Remove routing, cache, only stripper save method

	* v2.0
        * [Original Post by honorcode23](https://forums.alliedmods.net/showthread.php?t=127418)
</details>

* Require | 必要安裝
    1. [left4dhooks](https://forums.alliedmods.net/showthread.php?t=321696)
	2. [[INC] Multi Colors](https://forums.alliedmods.net/showthread.php?t=247770)
    3. [Stripper:Source](http://www.bailopan.net/stripper/#install)

* How to use
	* Type !admin to call adm menu and you will see "Spawn Objects" option
	* **Create Object**
        1. Admin types !admin in chat->Spawn Objects->Spawn Objects->Select the spawn method
        2. Physics（affected by gravity），Non-solid（you can go through it），Solid（won't be affected by gravity），Items&Weapons（Guns, Melees, Supplies, Throwables, etc.）

	* **Save Object**
        1. Admin types !admin in chat->Spawn Objects->Save Objects->Save Stripper File

* Why I can't read object spawn menu?
	* The data/l4d2_spawn_props_models.txt is Chinese language
	* Either you translate by yourself, or just download [english data](https://forums.alliedmods.net/showpost.php?p=2607756&postcount=178) here(but fewer models)

* How to add more models?
	* Modify data/l4d2_spawn_props_models.txt

* <details><summary>ConVar | 指令</summary>

	* cfg\sourcemod\l4d2_spawn_props.cfg
		```php
        // Enable the Decorative category
        l4d2_spawn_props_category_decorative "1"

        // Enable the Exterior category
        l4d2_spawn_props_category_exterior "1"

        // Enable the Foliage category
        l4d2_spawn_props_category_foliage "1"

        // Enable the Interior category
        l4d2_spawn_props_category_interior "1"

        // Enable the Misc category
        l4d2_spawn_props_category_misc "1"

        // Enable the Vehicles category
        l4d2_spawn_props_category_vehicles "1"

        // Enable the Dynamic (Non-solid) Objects in the menu
        l4d2_spawn_props_dynamic "1"

        // Enable the Items & Weapons Objects in the menu
        l4d2_spawn_props_items "1"

        // Log if an admin spawns an object?
        l4d2_spawn_props_log_actions "0"

        // Enable the Physics Objects in the menu
        l4d2_spawn_props_physics "1"

        // Enable the Static (Solid) Objects in the menu
        l4d2_spawn_props_static "1"
		```
</details>

* <details><summary>Command | 命令</summary>

	* **Spawns an object with the given information, sm_spawnprop <model> [static | dynamic | physics] [cursor | origin] (Adm required: ADMFLAG_UNBAN)**
		```php
		sm_spawnprop
		```

	* **Save all the spawned object in a stripper file, path: addons/stripper/maps/XXXX.cfg (XXXX is map name) (Adm required: ADMFLAG_UNBAN)**
		```php
		sm_savemap
		```

	* **Rotates the looking spawned object with the desired angles, Usage: sm_prop_rotate <axys> <angles> [EX: !prop_rotate x 30] (Adm required: ADMFLAG_UNBAN)**
		```php
		sm_prop_rotate
		```

	* **Remove last spawned object (Adm required: ADMFLAG_UNBAN)**
		```php
		sm_prop_removelast
		```

	* **Remove the looking object (Adm required: ADMFLAG_UNBAN)**
		```php
		sm_prop_removelook
		```

	* **Remove all spawned objects (Adm required: ADMFLAG_UNBAN)**
		```php
		sm_prop_removeall
		```

	* **Move the looking spawned object with the desired movement type, Usage: sm_prop_move <axys> <distance> [EX: !prop_move x 30] (Adm required: ADMFLAG_UNBAN)**
		```php
		sm_prop_move
		```

	* **Forces the looking spawned object angles, Usage: sm_prop_setang <X Y Z> [EX: !prop_setang 30 0 34] (Adm required: ADMFLAG_UNBAN)**
		```php
		sm_prop_setang
		```

	* **Sets the looking spawned object position, Usage: sm_prop_setpos <X Y Z> [EX: !prop_setpos 505 -34 17 (Adm required: ADMFLAG_UNBAN)**
		```php
		sm_prop_setpos
		```

	* **Locks the looking spawned object, Use for move and rotate (Adm required: ADMFLAG_UNBAN)**
		```php
		sm_prop_lock
		```

	* **Clone the last spawned object (Adm required: ADMFLAG_UNBAN)**
		```php
		sm_prop_clone
		```

	* **Print the looking object information (Adm required: ADMFLAG_UNBAN)**
		```php
		sm_prop_print
		```
</details>

- - - -
# 中文說明
創造屬於自己風格的地圖，製作迷宮與障礙物

* 如何創造物件?
    1. 管理員輸入!admin->生成物件->生成物件->選擇其中一項
    2. 動態（會受重力影響），穿透（擺好看），固態（不受重力影響），物品（槍械、近戰、醫療物品、投擲物品、彈藥堆、雷射裝置）

* 如何儲存物件?
    1. 管理員輸入!admin->生成物件->儲存物件

* 如何增加更多模組?
	* 編輯檔案 data/l4d2_spawn_props_models.txt




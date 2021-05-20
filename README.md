# Login system using Node.js, Express and MySQL


## Note for myself
Step 1: Install softwares we needed

1. Install `MySQL Community server` in the PC/server first. [Download MySQL](https://dev.mysql.com/downloads/file/?id=505134)

2. Install `node.js` in PC/server. [Download](https://nodejs.org/en/)

Step 2: Setting in `MySQL server`

1. Create db,
    ```sql
    CREATE DATABASE IF NOT EXISTS `nodelogin` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
    USE `nodelogin`;
    ```

2. Create table in that db,
    ```sql
    CREATE TABLE IF NOT EXISTS `accounts` (
    `id` int(11) NOT NULL,
    `username` varchar(50) NOT NULL,
    `password` varchar(255) NOT NULL,
    `email` varchar(100) NOT NULL
    ) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;
    ```

3. Add rows in the table,
    ```sql
    INSERT INTO `accounts` (`id`, `username`, `password`, `email`) VALUES (1, 'test', 'test', 'test@test.com');
    ```

4. 
    ```sql 
    ALTER TABLE `accounts` ADD PRIMARY KEY (`id`);
    ALTER TABLE `accounts` MODIFY `id` int(11) NOT NULL AUTO_INCREMENT,AUTO_INCREMENT=2;
    ```

Step 3: Setup project folder and JavaScript runtime environment.

`package.json`: `"dependencies"` shows all installed modules/libraries.

    NPM Install 到底做了些什麼？node_modules 檔案結構 + 特性入門:
    ==> https://ithelp.ithome.com.tw/articles/10191783

## Reference links
[Tutorial](https://codeshack.io/basic-login-system-nodejs-express-mysql/)
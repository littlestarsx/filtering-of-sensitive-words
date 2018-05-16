

##  安装&使用流程

### 安装扩展 

    composer require zuoan-link/filtering-of-sensitive-words      

   
#### 如果你需要手动引入

    require './vendor/autoload.php';
    
    use DfaFilter\SensitiveHelper;

### 实例化
    // get one helper
    $handle = new SensitiveHelper();
   
### 检测是否含有敏感词

    $islegal = $handle->islegal($content);
### 敏感词过滤
    
    // 敏感词替换为***为例
    $filterContent = $handle->replace($content, '***');
    
### 获取文字中的敏感词

    // 获取内容中所有的敏感词
    $sensitiveWordGroup = $handle->getBadWord($content);
    // 仅且获取一个敏感词
    $sensitiveWordGroup = $handle->getBadWord($content, 1);

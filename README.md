# spelling.js

<!-- ![](https://img.shields.io/badge/.NET-%3E%3D3.5-brightgreen.svg) -->
![](https://img.shields.io/badge/version-1.0.0-blue.svg)
![](https://img.shields.io/badge/license-Apache%20Licence%202.0-green.svg)

*spelling.js是使用javascript实现中文首拼和全拼的类库*
## 使用方法
+ 在`<head>`标签中引用    **/dist/spelling.min.js** 
+ 调用方法 `spelling.getFullSpell('咏鹅')` 和 `spelling.getFirstSpell('咏鹅')`
## 模板
    <!DOCTYPE html>
    <html>

    <head>
        <meta charset="utf-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <title>咏鹅</title>
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <script src="../dist/spelling.min.js"></script>
    </head>

    <body>
        <div>
            <p>
                <script>
                    spelling.options({fullSpellSeparate:'',fullCharCase:'upperCamelCase',firstCharCase:'lowerCase'});
                    document.write(spelling.getFullSpell('咏鹅'));
                </script>
            </p>
            <p>咏鹅</p>
            <p>
                <script>
                    document.write(spelling.getFullSpell('唐：骆宾王'));
                </script>
            </p>
            <p>唐：骆宾王</p>
            <p>
                <script>
                    document.write(spelling.getFullSpell('鹅，鹅，鹅，曲项向天歌'));
                </script>
            </p>
            <p>鹅，鹅，鹅，曲项向天歌</p>
            <p>
                <script>
                    document.write(spelling.getFullSpell('白毛浮绿水，红掌拨清波'));
                </script>
            </p>
            <p>白毛浮绿水，红掌拨清波</p>
        </div>
        
        <div>
                <p>
                    <script>
                        document.write(spelling.getFirstSpell('咏鹅'));
                    </script>
                </p>
                <p>咏鹅</p>
                <p>
                    <script>
                        document.write(spelling.getFirstSpell('唐：骆宾王'));
                    </script>
                </p>
                <p>唐：骆宾王</p>
                <p>
                    <script>
                        document.write(spelling.getFirstSpell('鹅，鹅，鹅，曲项向天歌'));
                    </script>
                </p>
                <p>鹅，鹅，鹅，曲项向天歌</p>
                <p>
                    <script>
                        document.write(spelling.getFirstSpell('白毛浮绿水，红掌拨清波'));
                    </script>
                </p>
                <p>白毛浮绿水，红掌拨清波</p>
            </div>
    </body>

    </html>
### 结果
    YongE

    咏鹅

    Tang：LuoBinWang

    唐：骆宾王

    E，E，E，QuXiangXiangTianGe

    鹅，鹅，鹅，曲项向天歌

    BaiMaoFuLvShui，HongZhangBoQingBo

    白毛浮绿水，红掌拨清波

    ye

    咏鹅

    t：lbw

    唐：骆宾王

    e，e，e，qxxtg

    鹅，鹅，鹅，曲项向天歌

    bmfls，hzbqb

    白毛浮绿水，红掌拨清波

## 属性


| 名称                | 描述   |类型   |默认值      |可选值|
| :----              | :---          | :----:     | :----:     |:----    |
| checkPolyphone |是否区分多音字   |  boolean   |  false  | true、false|
| fullSpellSeparate  |  拼音全拼间隔       |string |  空       |#、@、空格等|
| fullCharCase |拼音全拼大小写方式   |  string   |  lowerCase  |upperCase：大写<br>lowerCase：小写<br>upperCamelCase：大写驼峰<br>lowerCamelCase：小写驼峰|
| firstCharCase |拼音首拼大小写方式   |  string   |  upperCase  |upperCase：大写<br>lowerCase：小写|
## 方法


| 名称                | 描述   |类型   |参数      |
| :----              | :---          | :----:     | :----:     |
| options |设置   |  `object`   |  `{checkPolyphone: false, fullSpellSeparate: "",fullCharCase: "lowerCase", firstCharCase: "upperCase" }`  |
| getFirstSpell |获取拼音首拼   |  `function`   | string   |
| getFullSpell |获取拼音全拼   |  `function`   | string   |

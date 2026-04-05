

### for Class
#classAccessmodifier

|     | Assess Modifier | Description                                                                   |
| --- | --------------- | ----------------------------------------------------------------------------- |
| 1   | Interal         | Class is accessible within the same assembly                                  |
| 2   | public          | class is accessible in the same assembly and other assemblies                 |
| 3   | static          | class contains only static members only                                       |
| 4   | abstract        | class can additionally contains abstract methods                              |
| 5   | sealed          | sealed class can't be inherited                                               |
| 6   | partial         | multiple partial classes that have same name, are combined into single class. |
|     |                 |                                                                               |


#### for Field and Method
#fieldAccessModifier #MethodAccessModifier

|     | Access Modifier    | in same class | in child of same assembly | in other class of same assembly | in child of other assembly | In Other class at other assembly |
| --- | ------------------ | ------------- | ------------------------- | ------------------------------- | -------------------------- | -------------------------------- |
| 1   | Private            | Yes           | No                        | No                              | No                         | No                               |
| 2   | Protected          | Yes           | Yes                       | No                              | Yes                        | No                               |
| 3   | private protected  | Yes           | Yes                       | No                              | No                         | No                               |
| 4   | internal           | Yes           | Yes                       | Yes                             | No                         | No                               |
| 5   | protected internal | Yes           | Yes                       | Yes                             | Yes                        | No                               |
| 6   | public             | Yes           | Yes                       | Yes                             | Yes                        | No                               |



---
title: Objeto DBEngine (DAO)
TOCTitle: DBEngine Object
ms:assetid: ceaeb505-615e-37ba-4633-27240ef8c5de
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834506(v=office.15)
ms:contentKeyID: 48547792
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 479eff80d25279a1c5e918a3b639443ad3b25c6c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703682"
---
# <a name="dbengine-object-dao"></a>Objeto DBEngine (DAO)

**Aplica-se a**: Access 2013, o Office 2013

O objeto **DBEngine** é de nível superior no modelo de objeto DAO.

## <a name="remarks"></a>Comentários

O objeto **DBEngine** contém e controla todos os outros objetos na hierarquia de objetos DAO. Você não pode criar objetos **DBEngine** adicionais, e o objeto **DBEngine** não é um elemento de nenhuma coleção.

Com qualquer tipo de banco de dados ou conexão, você pode:

  - Usar a propriedade **Version** para obter o número de versão do DAO.

  - Usar a propriedade **LoginTimeout** para obter ou definir o tempo limite de login do ODBC e o método **RegisterDatabase** para fornecer as informações do ODBC ao mecanismo de banco de dados do Microsoft Access.

  - Usar as propriedades **DefaultPassword** e **DefaultUser** para definir a identificação do usuário e a senha para o objeto **Workspace** padrão.

  - Usar o método **CreateWorkspace** para criar um novo objeto **Workspace**. Você pode usar os argumentos opcionais para substituir as configurações das propriedades **DefaultType**, **DefaultPassword** e **DefaultUser**.

  - Usar o método **OpenDatabase** para abrir um banco de dados no **Workspace** padrão e usar os métodos **BeginTrans**, **Commit** e **Rollback** para controlar as transações no **Workspace** padrão.

  - Usar a coleção **Workspaces** para fazer referência a objetos **Workspace** específicos.

  - Usar a coleção **Errors** para examinar detalhes do erro de acesso aos dados.

Outras propriedades e métodos estão disponíveis apenas quando você utiliza o DAO com o mecanismo de banco de dados do Microsoft Access. Você pode usá-los para controlar o mecanismo de banco de dados do Microsoft Access, manipular suas propriedades e executar tarefas em objetos temporários que não são elementos das coleções. Por exemplo, você pode:

  - Usar o método **CreateDatabase** para criar um novo objeto **Database** do mecanismo de banco de dados do Microsoft Access.

  - Usar o método **Idle** para permitir que o mecanismo de banco de dados do Microsoft Access conclua qualquer tarefa pendente.

  - Usar os métodos **CompactDatabase** e **RepairDatabase** para manter arquivos de banco de dados.

  - Usar as propriedades **IniPath** e **SystemDB** para especificar o local das informações de Registro do Windows do mecanismo de banco de dados do Microsoft Access e o arquivo de informações do grupo de trabalho do Microsoft Access, respectivamente. O método **SetOption** permite substituir as configurações de Registro do Windows para o mecanismo de banco de dados do Microsoft Access.

Depois de alterar as configurações das propriedades **DefaultType** e **IniPath**, somente os objetos **Workspace** subsequentes refletirão essas alterações.

Para se referir a uma coleção que pertence ao objeto **DBEngine** ou para se referir a um método ou a uma propriedade que se aplique a esse objeto, use esta sintaxe:

\[**DBEngine**. \] \[coleção | método | propriedade\]

## <a name="example"></a>Exemplo

Este exemplo enumera as coleções do objeto **DBEngine**.

```vb
    Sub DBEngineX() 
     
     Dim wrkLoop As Workspace 
     Dim prpLoop As Property 
     
     With DBEngine 
     Debug.Print "DBEngine Properties" 
     
     ' Enumerate Properties collection of DBEngine, 
     ' trapping for properties whose values are 
     ' invalid in this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " _ 
     & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Debug.Print "Workspaces collection of DBEngine" 
     
     ' Enumerate Workspaces collection of DBEngine. 
     For Each wrkLoop In .Workspaces 
     Debug.Print " " & wrkLoop.Name 
     
     ' Enumerate Properties collection of each 
     ' Workspace object, trapping for properties 
     ' whose values are invalid in this context. 
     For Each prpLoop In wrkLoop.Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Next wrkLoop 
     
     End With 
     
    End Sub
```

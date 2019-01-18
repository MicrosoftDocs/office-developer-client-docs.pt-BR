---
title: Coleção Workspaces (DAO)
TOCTitle: Workspaces Collection
ms:assetid: 88b851ce-4180-964f-582e-bc9571bf554c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197057(v=office.15)
ms:contentKeyID: 48546142
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c615be9e92a936486c15377514c2b695f68bb5b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698411"
---
# <a name="workspaces-collection-dao"></a>Coleção Workspaces (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Uma coleção **Workspaces** contém todos os objetos **Workspace** ativos e não-ocultos do objeto **DBEngine**. (Objetos **Workspace** ocultos não são acrescentados à coleção e referenciados pela variável à qual são atribuídos.)

## <a name="remarks"></a>Comentários

Use o objeto **Workspace** para gerenciar a sessão atual ou para iniciar uma sessão adicional.

Quando você primeiro consultar ou usa um objeto **Workspace** , você cria o espaço de trabalho padrão, DBEngine.Workspaces(0) automaticamente. As configurações das propriedades **nome** e **nome de usuário** do espaço de trabalho padrão são "\#espaço de trabalho padrão\#" e "Admin", respectivamente. Se a segurança estiver ativada, a configuração da propriedade **UserName** é o nome do usuário que fez logon.

Você pode criar novos objetos **Workspace** com o método **[CreateWorkspace](dbengine-createworkspace-method-dao.md)**. Depois de criar um novo objeto **Workspace**, você deve acrescentá-lo à coleção **Workspaces** se precisar fazer referência a ele a partir da coleção **Workspaces**. Você pode, no entanto, usar um objeto **Workspace** recém-criado sem acrescentá-lo à coleção **Workspaces**.

Para fazer referência a um objeto **Workspace** em uma coleção por seu número ordinal ou por sua configuração de propriedade **Name**, use uma das seguintes formas de sintaxe:

**DBEngine**. **Espaços de trabalho** (0)

**DBEngine**. **Espaços de trabalho** ("nome")

**DBEngine**. **Espaços de trabalho** \! \[nome\]


> [!NOTE]
> [!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.



## <a name="example"></a>Exemplo

Este exemplo cria um novo objeto Microsoft Access Workspace e o acrescenta à coleção **Workspaces**. Em seguida, enumeram-se as coleções **Workspaces** e a coleção **Properties** de cada objeto **Workspace**.

```vb 
Sub WorkspaceX() 
 
 Dim wrkNewAcc As Workspace 
 Dim wrkLoop As Workspace 
 Dim prpLoop As Property 
 
 ' Create a new Microsoft Access workspace. 
 Set wrkNewAcc = CreateWorkspace("NewAccessWorkspace", _ 
 "admin", "", dbUseJet) 
 Workspaces.Append wrkNewAcc 
 
 ' Enumerate the Workspaces collection. 
 For Each wrkLoop In Workspaces 
 With wrkLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of the new 
 ' Workspace object. 
 For Each prpLoop In .Properties 
 On Error Resume Next 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 On Error GoTo 0 
 Next prpLoop 
 End With 
 Next wrkLoop 
 
 wrkNewAcc.Close 
End Sub 
```

<br/>

Este exemplo usa o método **CreateWorkspace** para criar um espaço de trabalho do Microsoft Access e um espaço de trabalho do ODBCDirect. Em seguida, listam-se as propriedades dos dois tipos de espaços de trabalho.

```vb 
Sub CreateWorkspaceX() 
 
 Dim wrkAcc As Workspace 
 Dim wrkLoop As Workspace 
 Dim prpLoop As Property 
 
 
 DefaultType = dbUseJet 
 ' Create an unnamed Workspace object of the type 
 ' specified by the DefaultType property of DBEngine 
 ' (dbUseJet). 
 Set wrkAcc = CreateWorkspace("", "admin", "") 
 
 ' Enumerate Workspaces collection. 
 Debug.Print "Workspace objects in Workspaces collection:" 
 For Each wrkLoop In Workspaces 
 Debug.Print " " & wrkLoop.Name 
 Next wrkLoop 
 
 With wrkAcc 
 ' Enumerate Properties collection of Microsoft Access 
 ' workspace. 
 Debug.Print _ 
 "Properties of unnamed Microsoft Access workspace" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 
 wrkAcc.Close 
 
End Sub 
 
```


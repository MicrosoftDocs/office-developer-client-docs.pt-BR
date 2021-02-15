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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308320"
---
# <a name="workspaces-collection-dao"></a>Coleção Workspaces (DAO)


**Aplica-se ao:** Access 2013, Office 2013

Uma coleção **Workspaces** contém todos os objetos **Workspace** ativos e não-ocultos do objeto **DBEngine**. (Objetos **Workspace** ocultos não são acrescentados à coleção e referenciados pela variável à qual são atribuídos.)

## <a name="remarks"></a>Comentários

Use o objeto **Workspace** para gerenciar a sessão atual ou para iniciar uma sessão adicional.

Quando se faz referência ou se usa um objeto **Workspace** pela primeira vez, cria-se automaticamente o espaço de trabalho padrão, DBEngine.Workspaces(0). As configurações das propriedades **Name** e **UserName** do espaço de trabalho padrão são "\#Default Workspace\#" e "Admin," respectivamente. Se a segurança estiver habilitada, a configuração da propriedade **UserName** é o nome do usuário conectado.

Você pode criar novos objetos **Workspace** com o método **[CreateWorkspace](dbengine-createworkspace-method-dao.md)**. Depois de criar um novo objeto **Workspace**, você deve acrescentá-lo à coleção **Workspaces** se precisar fazer referência a ele a partir da coleção **Workspaces**. Você pode, no entanto, usar um objeto **Workspace** recém-criado sem acrescentá-lo à coleção **Workspaces**.

Para referir-se a um objeto **Workspace** de uma coleção pelo número ordinal ou pela configuração da propriedade **Name**, use qualquer uma das formas de sintaxe a seguir:

**DBEngine**.**Workspaces**(0)

**DBEngine**.**Workspaces**("name")

**DBEngine**.**Workspaces**\!\[name\]


> [!NOTE]
> O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.



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

Este exemplo usa o método **CreateWorkspace** para criar um espaço de trabalho Microsoft Access. Em seguida, ele lista as propriedades dos dois tipos de espaço de trabalho.

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


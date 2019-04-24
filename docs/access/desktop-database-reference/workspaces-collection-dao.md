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
# <a name="workspaces-collection-dao"></a><span data-ttu-id="69857-102">Coleção Workspaces (DAO)</span><span class="sxs-lookup"><span data-stu-id="69857-102">Workspaces collection (DAO)</span></span>


<span data-ttu-id="69857-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69857-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69857-p101">Uma coleção **Workspaces** contém todos os objetos **Workspace** ativos e não-ocultos do objeto **DBEngine**. (Objetos **Workspace** ocultos não são acrescentados à coleção e referenciados pela variável à qual são atribuídos.)</span><span class="sxs-lookup"><span data-stu-id="69857-p101">A **Workspaces** collection contains all active, unhidden **Workspace** objects of the **DBEngine** object. (Hidden **Workspace** objects are not appended to the collection and referenced by the variable to which they are assigned.)</span></span>

## <a name="remarks"></a><span data-ttu-id="69857-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="69857-106">Remarks</span></span>

<span data-ttu-id="69857-107">Use o objeto **Workspace** para gerenciar a sessão atual ou para iniciar uma sessão adicional.</span><span class="sxs-lookup"><span data-stu-id="69857-107">Use the **Workspace** object to manage the current session or to start an additional session.</span></span>

<span data-ttu-id="69857-108">Quando você se referir ou usar um objeto **Workspace** pela primeira vez, crie automaticamente o espaço de trabalho padrão, DBEngine. Workspaces (0).</span><span class="sxs-lookup"><span data-stu-id="69857-108">When you first refer to or use a **Workspace** object, you automatically create the default workspace, DBEngine.Workspaces(0).</span></span> <span data-ttu-id="69857-109">As configurações das propriedades **Name** e **username** do espaço de trabalho padrão são "\#espaço de\#trabalho padrão" e "administrador", respectivamente.</span><span class="sxs-lookup"><span data-stu-id="69857-109">The settings of the **Name** and **UserName** properties of the default workspace are "\#Default Workspace\#" and "Admin," respectively.</span></span> <span data-ttu-id="69857-110">Se a segurança estiver ativada, a configuração da propriedade **UserName** é o nome do usuário que fez logon.</span><span class="sxs-lookup"><span data-stu-id="69857-110">If security is enabled, the **UserName** property setting is the name of the user who logged on.</span></span>

<span data-ttu-id="69857-p103">Você pode criar novos objetos **Workspace** com o método **[CreateWorkspace](dbengine-createworkspace-method-dao.md)**. Depois de criar um novo objeto **Workspace**, você deve acrescentá-lo à coleção **Workspaces** se precisar fazer referência a ele a partir da coleção **Workspaces**. Você pode, no entanto, usar um objeto **Workspace** recém-criado sem acrescentá-lo à coleção **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="69857-p103">You can create new **Workspace** objects with the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method. After you create a new **Workspace** object, you must append it to the **Workspaces** collection if you need to refer to it from the **Workspaces** collection. You can, however, use a newly created **Workspace** object without appending it to the **Workspaces** collection.</span></span>

<span data-ttu-id="69857-114">Para fazer referência a um objeto **Workspace** em uma coleção por seu número ordinal ou por sua configuração de propriedade **Name**, use uma das seguintes formas de sintaxe:</span><span class="sxs-lookup"><span data-stu-id="69857-114">To refer to a **Workspace** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="69857-115">**DBEngine**. **Espaços de trabalho** ,0</span><span class="sxs-lookup"><span data-stu-id="69857-115">**DBEngine**.**Workspaces**(0)</span></span>

<span data-ttu-id="69857-116">**DBEngine**. **Espaços de trabalho** ("Name")</span><span class="sxs-lookup"><span data-stu-id="69857-116">**DBEngine**.**Workspaces**("name")</span></span>

<span data-ttu-id="69857-117">**DBEngine**. **Espaços de trabalho** \! \[nome\]</span><span class="sxs-lookup"><span data-stu-id="69857-117">**DBEngine**.**Workspaces**\!\[name\]</span></span>


> [!NOTE]
> <span data-ttu-id="69857-p104">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="69857-p104">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>



## <a name="example"></a><span data-ttu-id="69857-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="69857-120">Example</span></span>

<span data-ttu-id="69857-p105">Este exemplo cria um novo objeto Microsoft Access Workspace e o acrescenta à coleção **Workspaces**. Em seguida, enumeram-se as coleções **Workspaces** e a coleção **Properties** de cada objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="69857-p105">This example creates a new Microsoft Access Workspace object and appends it to the **Workspaces** collection. It then enumerates the **Workspaces** collections and the **Properties** collection of the **Workspace** object.</span></span>

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

<span data-ttu-id="69857-p106">Este exemplo usa o método **CreateWorkspace** para criar um espaço de trabalho Microsoft Access. Em seguida, ele lista as propriedades dos dois tipos de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="69857-p106">This example uses the **CreateWorkspace** method to create a Microsoft Access workspace. It then lists the properties of theworkspace.</span></span>

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


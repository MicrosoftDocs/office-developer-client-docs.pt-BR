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
# <a name="dbengine-object-dao"></a><span data-ttu-id="bd99e-102">Objeto DBEngine (DAO)</span><span class="sxs-lookup"><span data-stu-id="bd99e-102">DBEngine object (DAO)</span></span>

<span data-ttu-id="bd99e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd99e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bd99e-104">O objeto **DBEngine** é de nível superior no modelo de objeto DAO.</span><span class="sxs-lookup"><span data-stu-id="bd99e-104">The **DBEngine** object is the top level object in the DAO object model.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd99e-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd99e-105">Remarks</span></span>

<span data-ttu-id="bd99e-p101">O objeto **DBEngine** contém e controla todos os outros objetos na hierarquia de objetos DAO. Você não pode criar objetos **DBEngine** adicionais, e o objeto **DBEngine** não é um elemento de nenhuma coleção.</span><span class="sxs-lookup"><span data-stu-id="bd99e-p101">The **DBEngine** object contains and controls all other objects in the hierarchy of DAO objects. You can't create additional **DBEngine** objects, and the **DBEngine** object isn't an element of any collection.</span></span>

<span data-ttu-id="bd99e-108">Com qualquer tipo de banco de dados ou conexão, você pode:</span><span class="sxs-lookup"><span data-stu-id="bd99e-108">With any type of database or connection, you can:</span></span>

  - <span data-ttu-id="bd99e-109">Usar a propriedade **Version** para obter o número de versão do DAO.</span><span class="sxs-lookup"><span data-stu-id="bd99e-109">Use the **Version** property to obtain the DAO version number.</span></span>

  - <span data-ttu-id="bd99e-110">Usar a propriedade **LoginTimeout** para obter ou definir o tempo limite de login do ODBC e o método **RegisterDatabase** para fornecer as informações do ODBC ao mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bd99e-110">Use the **LoginTimeout** property to obtain or set the ODBC login timeout, and the **RegisterDatabase** method to provide ODBC information to the Microsoft Access database engine.</span></span>

  - <span data-ttu-id="bd99e-111">Usar as propriedades **DefaultPassword** e **DefaultUser** para definir a identificação do usuário e a senha para o objeto **Workspace** padrão.</span><span class="sxs-lookup"><span data-stu-id="bd99e-111">Use the **DefaultPassword** and **DefaultUser** properties to set the user identification and password for the default **Workspace** object.</span></span>

  - <span data-ttu-id="bd99e-p102">Usar o método **CreateWorkspace** para criar um novo objeto **Workspace**. Você pode usar os argumentos opcionais para substituir as configurações das propriedades **DefaultType**, **DefaultPassword** e **DefaultUser**.</span><span class="sxs-lookup"><span data-stu-id="bd99e-p102">Use the **CreateWorkspace** method to create a new **Workspace** object. You can use optional arguments to override the settings of the **DefaultType**, **DefaultPassword**, and **DefaultUser** properties.</span></span>

  - <span data-ttu-id="bd99e-114">Usar o método **OpenDatabase** para abrir um banco de dados no **Workspace** padrão e usar os métodos **BeginTrans**, **Commit** e **Rollback** para controlar as transações no **Workspace** padrão.</span><span class="sxs-lookup"><span data-stu-id="bd99e-114">Use the **OpenDatabase** method to open a database in the default **Workspace**, and use the **BeginTrans**, **Commit**, and **Rollback** methods to control transactions on the default **Workspace**.</span></span>

  - <span data-ttu-id="bd99e-115">Usar a coleção **Workspaces** para fazer referência a objetos **Workspace** específicos.</span><span class="sxs-lookup"><span data-stu-id="bd99e-115">Use the **Workspaces** collection to reference specific **Workspace** objects.</span></span>

  - <span data-ttu-id="bd99e-116">Usar a coleção **Errors** para examinar detalhes do erro de acesso aos dados.</span><span class="sxs-lookup"><span data-stu-id="bd99e-116">Use the **Errors** collection to examine data access error details.</span></span>

<span data-ttu-id="bd99e-p103">Outras propriedades e métodos estão disponíveis apenas quando você utiliza o DAO com o mecanismo de banco de dados do Microsoft Access. Você pode usá-los para controlar o mecanismo de banco de dados do Microsoft Access, manipular suas propriedades e executar tarefas em objetos temporários que não são elementos das coleções. Por exemplo, você pode:</span><span class="sxs-lookup"><span data-stu-id="bd99e-p103">Other properties and methods are only available when you use DAO with the Microsoft Access database engine. You can use them to control the Microsoft Access database engine, manipulate its properties, and perform tasks on temporary objects that aren't elements of collections. For example, you can:</span></span>

  - <span data-ttu-id="bd99e-120">Usar o método **CreateDatabase** para criar um novo objeto **Database** do mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bd99e-120">Use the **CreateDatabase** method to create a new Microsoft Access database engine **Database** object.</span></span>

  - <span data-ttu-id="bd99e-121">Usar o método **Idle** para permitir que o mecanismo de banco de dados do Microsoft Access conclua qualquer tarefa pendente.</span><span class="sxs-lookup"><span data-stu-id="bd99e-121">Use the **Idle** method to enable the Microsoft Access database engine to complete any pending tasks.</span></span>

  - <span data-ttu-id="bd99e-122">Usar os métodos **CompactDatabase** e **RepairDatabase** para manter arquivos de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bd99e-122">Use the **CompactDatabase** and **RepairDatabase** methods to maintain database files.</span></span>

  - <span data-ttu-id="bd99e-p104">Usar as propriedades **IniPath** e **SystemDB** para especificar o local das informações de Registro do Windows do mecanismo de banco de dados do Microsoft Access e o arquivo de informações do grupo de trabalho do Microsoft Access, respectivamente. O método **SetOption** permite substituir as configurações de Registro do Windows para o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bd99e-p104">Use the **IniPath** and **SystemDB** properties to specify the location of Microsoft Access database engine Windows Registry information and the Microsoft Access workgroup information file, respectively. The **SetOption** method allows you override windows registry settings for the Microsoft Access database engine.</span></span>

<span data-ttu-id="bd99e-125">Depois de alterar as configurações das propriedades **DefaultType** e **IniPath**, somente os objetos **Workspace** subsequentes refletirão essas alterações.</span><span class="sxs-lookup"><span data-stu-id="bd99e-125">After you change the **DefaultType** and **IniPath** property settings, only subsequent **Workspace** objects will reflect these changes.</span></span>

<span data-ttu-id="bd99e-126">Para se referir a uma coleção que pertence ao objeto **DBEngine** ou para se referir a um método ou a uma propriedade que se aplique a esse objeto, use esta sintaxe:</span><span class="sxs-lookup"><span data-stu-id="bd99e-126">To refer to a collection that belongs to the **DBEngine** object, or to refer to a method or property that applies to this object, use this syntax:</span></span>

<span data-ttu-id="bd99e-127">\[**DBEngine**. \] \[coleção | método | propriedade\]</span><span class="sxs-lookup"><span data-stu-id="bd99e-127">\[**DBEngine**.\]\[collection | method | property\]</span></span>

## <a name="example"></a><span data-ttu-id="bd99e-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bd99e-128">Example</span></span>

<span data-ttu-id="bd99e-129">Este exemplo enumera as coleções do objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="bd99e-129">This example enumerates the collections of the **DBEngine** object.</span></span>

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

---
title: Método DBEngine.CreateWorkspace (DAO)
TOCTitle: CreateWorkspace Method
ms:assetid: a7d73771-9420-0448-99e6-d6c4aa78683a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821374(v=office.15)
ms:contentKeyID: 48546888
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052966
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 730c7bb6b659d0743613c590e3683b92fe7f0d65
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929248"
---
# <a name="dbenginecreateworkspace-method-dao"></a><span data-ttu-id="8defe-102">Método DBEngine.CreateWorkspace (DAO)</span><span class="sxs-lookup"><span data-stu-id="8defe-102">DBEngine.CreateWorkspace method (DAO)</span></span>


<span data-ttu-id="8defe-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8defe-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="8defe-104">Cria um novo objeto **[Workspace](workspace-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="8defe-104">Creates a new **[Workspace](workspace-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8defe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8defe-105">Syntax</span></span>

<span data-ttu-id="8defe-106">*expressão* . CreateWorkspace (***nome***, ***nome de usuário***, ***senha***, ***UseType***)</span><span class="sxs-lookup"><span data-stu-id="8defe-106">*expression* .CreateWorkspace(***Name***, ***UserName***, ***Password***, ***UseType***)</span></span>

<span data-ttu-id="8defe-107">*expressão* Uma variável que representa um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="8defe-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="8defe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8defe-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8defe-109">Nome</span><span class="sxs-lookup"><span data-stu-id="8defe-109">Name</span></span></p></th>
<th><p><span data-ttu-id="8defe-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="8defe-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="8defe-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8defe-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="8defe-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8defe-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8defe-113">Name</span><span class="sxs-lookup"><span data-stu-id="8defe-113">Name</span></span></p></td>
<td><p><span data-ttu-id="8defe-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8defe-114">Required</span></span></p></td>
<td><p><span data-ttu-id="8defe-115"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="8defe-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8defe-p101">Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Workspace</strong>. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter detalhes sobre nomes válidos de <strong>Workspace</strong>.</span><span class="sxs-lookup"><span data-stu-id="8defe-p101">A <strong>String</strong> that uniquely names the new <strong>Workspace</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Workspace</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8defe-118">UserName</span><span class="sxs-lookup"><span data-stu-id="8defe-118">UserName</span></span></p></td>
<td><p><span data-ttu-id="8defe-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8defe-119">Required</span></span></p></td>
<td><p><span data-ttu-id="8defe-120"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="8defe-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8defe-p102">Um <strong>String</strong> que identifica o proprietário do novo objeto <strong>Workspace</strong>. Consulte a propriedade <strong>UserName</strong> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8defe-p102">A <strong>String</strong> that identifies the owner of the new <strong>Workspace</strong> object. See the <strong>UserName</strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8defe-123">Senha</span><span class="sxs-lookup"><span data-stu-id="8defe-123">Password</span></span></p></td>
<td><p><span data-ttu-id="8defe-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8defe-124">Required</span></span></p></td>
<td><p><span data-ttu-id="8defe-125"><strong>Cadeia de caracteres</strong></span><span class="sxs-lookup"><span data-stu-id="8defe-125"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8defe-126">Uma <strong>cadeia de caracteres</strong> contendo a senha para o novo objeto <strong>Workspace</strong> .</span><span class="sxs-lookup"><span data-stu-id="8defe-126">A <strong>String</strong> containing the password for the new <strong>Workspace</strong> object.</span></span> <span data-ttu-id="8defe-127">A senha pode ter até 20 caracteres e pode incluir qualquer caractere exceto o caractere ASCII 0 (nulo).</span><span class="sxs-lookup"><span data-stu-id="8defe-127">The password can be up to 20 characters long and can include any characters except ASCII character 0 (null).</span></span></p>

> [!NOTE]
> <span data-ttu-id="8defe-p104">[!OBSERVAçãO] Use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos. As senhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: House27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</span><span class="sxs-lookup"><span data-stu-id="8defe-p104">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8defe-133">UseType</span><span class="sxs-lookup"><span data-stu-id="8defe-133">UseType</span></span></p></td>
<td><p><span data-ttu-id="8defe-134">Opcional</span><span class="sxs-lookup"><span data-stu-id="8defe-134">Optional</span></span></p></td>
<td><p><span data-ttu-id="8defe-135"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8defe-135"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8defe-136">Um dos valores <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="8defe-136">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>

> [!NOTE]
> <span data-ttu-id="8defe-137">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="8defe-137">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="8defe-138">Definindo o argumento type como **dbUseODBC** resultará em um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="8defe-138">Setting the type argument to **dbUseODBC** will result in a run-time error.</span></span> <span data-ttu-id="8defe-139">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8defe-139">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="8defe-140">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8defe-140">Return value</span></span>

<span data-ttu-id="8defe-141">Workspace</span><span class="sxs-lookup"><span data-stu-id="8defe-141">Workspace</span></span>

## <a name="remarks"></a><span data-ttu-id="8defe-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="8defe-142">Remarks</span></span>

<span data-ttu-id="8defe-143">Após usar o método **CreateWorkspace** para criar um novo objeto **Workspace**, uma sessão do **Workspace** será iniciada e você poderá fazer referência ao objeto **Workspace** em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8defe-143">Once you use the **CreateWorkspace** method to create a new **Workspace** object, a **Workspace** session is started, and you can refer to the **Workspace** object in your application.</span></span>

<span data-ttu-id="8defe-p106">Objetos **Workspace** não são permanentes e não podem ser salvos em disco. Após criar um objeto **Workspace**, você não poderá alterar suas configurações de propriedade, com exceção da propriedade **Name**, que você pode modificar antes de acrescentar o objeto **Workspace** à coleção **[Workspaces](workspaces-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="8defe-p106">**Workspace** objects aren't permanent, and you can't save them to disk. Once you create a **Workspace** object, you can't alter any of its property settings, except for the **Name** property, which you can modify before appending the **Workspace** object to the **[Workspaces](workspaces-collection-dao.md)** collection.</span></span>

<span data-ttu-id="8defe-p107">Não é necessário acrescentar o novo objeto **Workspace** à coleção antes de usá-la. Acrescenta-se um objeto **Workspace** recém-criado apenas se for preciso fazer referência a ele por meio da coleção **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="8defe-p107">You don't have to append the new **Workspace** object to a collection before you can use it. You append a newly created **Workspace** object only if you need to refer to it through the **Workspaces** collection.</span></span>

<span data-ttu-id="8defe-148">Para remover um objeto **Workspace** da coleção **Workspaces**, feche todos os bancos de dados e conexões abertos e use o método **[Close](connection-close-method-dao.md)** no objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="8defe-148">To remove a **Workspace** object from the **Workspaces** collection, close all open databases and connections and then use the **[Close](connection-close-method-dao.md)** method on the **Workspace** object.</span></span>

## <a name="example"></a><span data-ttu-id="8defe-149">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8defe-149">Example</span></span>

<span data-ttu-id="8defe-p108">Este exemplo usa o método **CreateWorkspace** para criar um espaço de trabalho do Microsoft Access Em seguida, lista as propriedades do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8defe-p108">This example uses the **CreateWorkspace** method to createMicrosoft Access workspace. It then lists the properties of the workspace.</span></span>

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
      Debug.Print "  " & wrkLoop.Name 
   Next wrkLoop 
 
   With wrkAcc 
      ' Enumerate Properties collection of Microsoft Access  
      ' workspace. 
      Debug.Print _ 
         "Properties of unnamed Microsoft Access workspace" 
      On Error Resume Next 
      For Each prpLoop In .Properties 
         Debug.Print "  " & prpLoop.Name & " = " & prpLoop 
      Next prpLoop 
      On Error GoTo 0 
   End With 
 
   wrkAcc.Close 
 
End Sub 
 
```


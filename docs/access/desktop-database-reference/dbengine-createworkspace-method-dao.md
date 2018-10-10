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
ms.openlocfilehash: 039da9aeb6166b25b0800533f50aa7ec5053c3c7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462005"
---
# <a name="dbenginecreateworkspace-method-dao"></a><span data-ttu-id="0f6d6-102">Método DBEngine.CreateWorkspace (DAO)</span><span class="sxs-lookup"><span data-stu-id="0f6d6-102">DBEngine.CreateWorkspace Method (DAO)</span></span>


<span data-ttu-id="0f6d6-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f6d6-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="0f6d6-104">Cria um novo objeto **[Workspace](workspace-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-104">Creates a new **[Workspace](workspace-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f6d6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f6d6-105">Syntax</span></span>

<span data-ttu-id="0f6d6-106">*expressão* . CreateWorkspace (***nome***, ***nome de usuário***, ***senha***, ***UseType***)</span><span class="sxs-lookup"><span data-stu-id="0f6d6-106">*expression* .CreateWorkspace(***Name***, ***UserName***, ***Password***, ***UseType***)</span></span>

<span data-ttu-id="0f6d6-107">*expressão* Uma variável que representa um objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="0f6d6-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="0f6d6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f6d6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0f6d6-109">Nome</span><span class="sxs-lookup"><span data-stu-id="0f6d6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0f6d6-110">Obrigatório/Opcional</span><span class="sxs-lookup"><span data-stu-id="0f6d6-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="0f6d6-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0f6d6-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="0f6d6-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f6d6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f6d6-113">Name</span><span class="sxs-lookup"><span data-stu-id="0f6d6-113">Name</span></span></p></td>
<td><p><span data-ttu-id="0f6d6-114">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0f6d6-114">Required</span></span></p></td>
<td><p><span data-ttu-id="0f6d6-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="0f6d6-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="0f6d6-p101">Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Workspace</strong>. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter detalhes sobre nomes válidos de <strong>Workspace</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-p101">A <strong>String</strong> that uniquely names the new <strong>Workspace</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Workspace</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f6d6-118">UserName</span><span class="sxs-lookup"><span data-stu-id="0f6d6-118">UserName</span></span></p></td>
<td><p><span data-ttu-id="0f6d6-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0f6d6-119">Required</span></span></p></td>
<td><p><span data-ttu-id="0f6d6-120"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="0f6d6-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="0f6d6-p102">Um <strong>String</strong> que identifica o proprietário do novo objeto <strong>Workspace</strong>. Consulte a propriedade <strong>UserName</strong> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-p102">A <strong>String</strong> that identifies the owner of the new <strong>Workspace</strong> object. See the <strong>UserName</strong> property for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f6d6-123">Senha</span><span class="sxs-lookup"><span data-stu-id="0f6d6-123">Password</span></span></p></td>
<td><p><span data-ttu-id="0f6d6-124">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0f6d6-124">Required</span></span></p></td>
<td><p><span data-ttu-id="0f6d6-125"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="0f6d6-125"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="0f6d6-126">Uma <strong>cadeia de caracteres</strong> contendo a senha para o novo objeto <strong>Workspace</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f6d6-126">A <strong>String</strong> containing the password for the new <strong>Workspace</strong> object.</span></span> <span data-ttu-id="0f6d6-127">A senha pode ter até 20 caracteres e pode incluir qualquer caractere exceto o caractere ASCII 0 (nulo).</span><span class="sxs-lookup"><span data-stu-id="0f6d6-127">The password can be up to 20 characters long and can include any characters except ASCII character 0 (null).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="0f6d6-p104">[!OBSERVAçãO] Use senhas fortes que combinem letras maiúsculas e minúsculas, números e símbolos. As senhas fracas não combinam esses elementos. Senha forte: Y6dh!et5. Senha fraca: House27. Use uma senha fraca para que você possa lembrá-la sem precisar escrevê-la.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-p104">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f6d6-133">UseType</span><span class="sxs-lookup"><span data-stu-id="0f6d6-133">UseType</span></span></p></td>
<td><p><span data-ttu-id="0f6d6-134">Opcional</span><span class="sxs-lookup"><span data-stu-id="0f6d6-134">Optional</span></span></p></td>
<td><p><span data-ttu-id="0f6d6-135"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0f6d6-135"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0f6d6-136">Um dos valores <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="0f6d6-136">One of the <strong><a href="workspacetypeenum-enumeration-dao.md">WorkspaceTypeEnum</a></strong> values.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="0f6d6-137">[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-137">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="0f6d6-138">Definindo o argumento type como <STRONG>dbUseODBC</STRONG> resultará em um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-138">Setting the type argument to <STRONG>dbUseODBC</STRONG> will result in a run-time error.</span></span> <span data-ttu-id="0f6d6-139">Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-139">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="0f6d6-140">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0f6d6-140">Return Value</span></span>

<span data-ttu-id="0f6d6-141">Workspace</span><span class="sxs-lookup"><span data-stu-id="0f6d6-141">Workspace</span></span>

## <a name="remarks"></a><span data-ttu-id="0f6d6-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f6d6-142">Remarks</span></span>

<span data-ttu-id="0f6d6-143">Após usar o método **CreateWorkspace** para criar um novo objeto **Workspace**, uma sessão do **Workspace** será iniciada e você poderá fazer referência ao objeto **Workspace** em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-143">Once you use the **CreateWorkspace** method to create a new **Workspace** object, a **Workspace** session is started, and you can refer to the **Workspace** object in your application.</span></span>

<span data-ttu-id="0f6d6-p106">Objetos **Workspace** não são permanentes e não podem ser salvos em disco. Após criar um objeto **Workspace**, você não poderá alterar suas configurações de propriedade, com exceção da propriedade **Name**, que você pode modificar antes de acrescentar o objeto **Workspace** à coleção **[Workspaces](workspaces-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-p106">**Workspace** objects aren't permanent, and you can't save them to disk. Once you create a **Workspace** object, you can't alter any of its property settings, except for the **Name** property, which you can modify before appending the **Workspace** object to the **[Workspaces](workspaces-collection-dao.md)** collection.</span></span>

<span data-ttu-id="0f6d6-p107">Não é necessário acrescentar o novo objeto **Workspace** à coleção antes de usá-la. Acrescenta-se um objeto **Workspace** recém-criado apenas se for preciso fazer referência a ele por meio da coleção **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-p107">You don't have to append the new **Workspace** object to a collection before you can use it. You append a newly created **Workspace** object only if you need to refer to it through the **Workspaces** collection.</span></span>

<span data-ttu-id="0f6d6-148">Para remover um objeto **Workspace** da coleção **Workspaces**, feche todos os bancos de dados e conexões abertos e use o método **[Close](connection-close-method-dao.md)** no objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-148">To remove a **Workspace** object from the **Workspaces** collection, close all open databases and connections and then use the **[Close](connection-close-method-dao.md)** method on the **Workspace** object.</span></span>

## <a name="example"></a><span data-ttu-id="0f6d6-149">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0f6d6-149">Example</span></span>

<span data-ttu-id="0f6d6-p108">Este exemplo usa o método **CreateWorkspace** para criar um espaço de trabalho do Microsoft Access Em seguida, lista as propriedades do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0f6d6-p108">This example uses the **CreateWorkspace** method to createMicrosoft Access workspace. It then lists the properties of the workspace.</span></span>

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


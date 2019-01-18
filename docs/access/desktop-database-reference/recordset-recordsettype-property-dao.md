---
title: Propriedade Recordset.RecordsetType (DAO)
TOCTitle: RecordsetType Property
ms:assetid: a66d4043-08cc-ead1-f9ff-efc7d7ea21bf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821178(v=office.15)
ms:contentKeyID: 48546853
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13361
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 64f7dda8bec7806ef510d265deab350dc3cdad6b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709653"
---
# <a name="recordsetrecordsettype-property-dao"></a><span data-ttu-id="d6b25-102">Propriedade Recordset.RecordsetType (DAO)</span><span class="sxs-lookup"><span data-stu-id="d6b25-102">Recordset.RecordsetType property (DAO)</span></span>

<span data-ttu-id="d6b25-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6b25-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d6b25-p101">Você pode utilizar a propriedade **RecordsetType** para especificar o tipo de conjunto de registros que estará disponível para um formulário. **Byte** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d6b25-p101">You can use the **RecordsetType** property to specify what kind of recordset is made available to a form. Read/write **Byte**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6b25-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6b25-106">Syntax</span></span>

<span data-ttu-id="d6b25-107">*expressão* . RecordsetType</span><span class="sxs-lookup"><span data-stu-id="d6b25-107">*expression* .RecordsetType</span></span>

<span data-ttu-id="d6b25-108">*expression* Uma variável que representa um objeto **Form**.</span><span class="sxs-lookup"><span data-stu-id="d6b25-108">*expression* A variable that represents a **Form** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6b25-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6b25-109">Remarks</span></span>

<span data-ttu-id="d6b25-110">A propriedade **RecordsetType** utiliza as configurações a seguir em um banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="d6b25-110">The **RecordsetType** property uses the following settings in a Microsoft Access database.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6b25-111">Configuração</span><span class="sxs-lookup"><span data-stu-id="d6b25-111">Setting</span></span></p></th>
<th><p><span data-ttu-id="d6b25-112">Tipo de conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="d6b25-112">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="d6b25-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6b25-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6b25-114">0</span><span class="sxs-lookup"><span data-stu-id="d6b25-114">0</span></span></p></td>
<td><p><span data-ttu-id="d6b25-115">Dynaset</span><span class="sxs-lookup"><span data-stu-id="d6b25-115">Dynaset</span></span></p></td>
<td><p><span data-ttu-id="d6b25-116">(Padrão) Você pode editar controles vinculados, com base em uma única tabela ou tabelas com um relacionamento individual.</span><span class="sxs-lookup"><span data-stu-id="d6b25-116">(Default) You can edit bound controls based on a single table or tables with a one-to-one relationship.</span></span> <span data-ttu-id="d6b25-117">Para controles ligados aos campos baseados em tabelas com uma relação um-para-muitos, você não pode editar dados do campo de ingresso no &quot;um&quot; lado do relacionamento, a menos que propagar atualização está habilitada entre as tabelas.</span><span class="sxs-lookup"><span data-stu-id="d6b25-117">For controls bound to fields based on tables with a one-to-many relationship, you can't edit data from the join field on the &quot;one&quot; side of the relationship unless cascade update is enabled between the tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6b25-118">1</span><span class="sxs-lookup"><span data-stu-id="d6b25-118">1</span></span></p></td>
<td><p><span data-ttu-id="d6b25-119">Dynaset (Atualizações inconsistentes)</span><span class="sxs-lookup"><span data-stu-id="d6b25-119">Dynaset (Inconsistent Updates)</span></span></p></td>
<td><p><span data-ttu-id="d6b25-120">Todas as tabelas e os controles ligados aos respectivos campos podem ser editados.</span><span class="sxs-lookup"><span data-stu-id="d6b25-120">All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d6b25-121">2</span><span class="sxs-lookup"><span data-stu-id="d6b25-121">2</span></span></p></td>
<td><p><span data-ttu-id="d6b25-122">Instantâneo</span><span class="sxs-lookup"><span data-stu-id="d6b25-122">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="d6b25-123">Não é possível editar as tabelas nem os controles ligados aos respectivos campos.</span><span class="sxs-lookup"><span data-stu-id="d6b25-123">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d6b25-124">[!OBSERVAçãO] Se não desejar que dados em controles ligados sejam editados quando um formulário estiver no modo Formulário ou no modo Folha de Dados, você poderá definir a propriedade **RecordsetType** como 2.</span><span class="sxs-lookup"><span data-stu-id="d6b25-124">If you don't want data in bound controls to be edited when a form is in Form view or Datasheet view, you can set the **RecordsetType** property to 2.</span></span>

<span data-ttu-id="d6b25-125">A propriedade **RecordsetType** utiliza as configurações a seguir em um projeto do Microsoft Access (.adp).</span><span class="sxs-lookup"><span data-stu-id="d6b25-125">The **RecordsetType** property uses the following settings in a Microsoft Access project (.adp).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6b25-126">Configuração</span><span class="sxs-lookup"><span data-stu-id="d6b25-126">Setting</span></span></p></th>
<th><p><span data-ttu-id="d6b25-127">Tipo de conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="d6b25-127">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="d6b25-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6b25-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6b25-129">3</span><span class="sxs-lookup"><span data-stu-id="d6b25-129">3</span></span></p></td>
<td><p><span data-ttu-id="d6b25-130">Instantâneo</span><span class="sxs-lookup"><span data-stu-id="d6b25-130">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="d6b25-131">Não é possível editar as tabelas nem os controles ligados aos respectivos campos.</span><span class="sxs-lookup"><span data-stu-id="d6b25-131">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6b25-132">4</span><span class="sxs-lookup"><span data-stu-id="d6b25-132">4</span></span></p></td>
<td><p><span data-ttu-id="d6b25-133">Instantâneo atualizável</span><span class="sxs-lookup"><span data-stu-id="d6b25-133">Updatable Snapshot</span></span></p></td>
<td><p><span data-ttu-id="d6b25-134">(Padrão) Todas as tabelas e os controles ligados aos respectivos campos podem ser editados.</span><span class="sxs-lookup"><span data-stu-id="d6b25-134">(Default) All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d6b25-135">[!OBSERVAçãO] Alterar a propriedade **RecordsetType** de um formulário ou de um relatório aberto resulta na recriação automática do conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="d6b25-135">Changing the **RecordsetType** property of an open form or report causes an automatic recreation of the recordset.</span></span>

<span data-ttu-id="d6b25-p103">Você pode criar formulários com base em várias tabelas base com campos ligados a controles nos formulários. Dependendo da configuração da propriedade **RecordsetType**, você poderá limitar os controles ligados a serem editados.</span><span class="sxs-lookup"><span data-stu-id="d6b25-p103">You can create forms based on multiple underlying tables with fields bound to controls on the forms. Depending on the **RecordsetType** property setting, you can limit which of these bound controls can be edited.</span></span>

<span data-ttu-id="d6b25-138">Além do controle de edição fornecido pelo **TipoDeConjuntoDeRegistros**, cada controle em um formulário tem uma propriedade **Locked** que você pode definir para especificar se o controle e seus dados base podem ser editados.</span><span class="sxs-lookup"><span data-stu-id="d6b25-138">In addition to the editing control provided by **RecordsetType**, each control on a form has a **Locked** property that you can set to specify whether the control and its underlying data can be edited.</span></span> <span data-ttu-id="d6b25-139">Se a propriedade **Locked** estiver definida como Sim, você não poderá editar os dados.</span><span class="sxs-lookup"><span data-stu-id="d6b25-139">If the **Locked** property is set to Yes, you can't edit the data.</span></span>

## <a name="example"></a><span data-ttu-id="d6b25-140">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d6b25-140">Example</span></span>

<span data-ttu-id="d6b25-p105">No exemplo a seguir, os registros somente poderão ser atualizados se a identificação do usuário for ADMIN. Este exemplo de código definirá a propriedade **RecordsetType** como Snapshot se o valor gstrUserID da variável pública for diferente de ADMIN.</span><span class="sxs-lookup"><span data-stu-id="d6b25-p105">In the following example, only if the user ID is ADMIN can records be updated. This code sample sets the **RecordsetType** property to Snapshot if the public variable gstrUserID value is not ADMIN.</span></span>

```vb
    Sub Form_Open(Cancel As Integer) 
     Const conSnapshot = 2 
     If gstrUserID <> "ADMIN" Then 
     Forms!Employees.RecordsetType = conSnapshot 
     End If 
    End Sub
```

## <a name="see-also"></a><span data-ttu-id="d6b25-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6b25-143">See also</span></span>

- [<span data-ttu-id="d6b25-144">Objeto Form</span><span class="sxs-lookup"><span data-stu-id="d6b25-144">Form Object</span></span>](https://docs.microsoft.com/office/vba/api/Access.Form)



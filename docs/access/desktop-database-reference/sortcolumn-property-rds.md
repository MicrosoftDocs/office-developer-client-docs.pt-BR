---
title: Propriedade SortColumn (RDS)
TOCTitle: SortColumn property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 61d31ba6044448d2b2534d6affa6157765e9cbc7
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949632"
---
# <a name="sortcolumn-property-rds"></a><span data-ttu-id="8b352-102">Propriedade SortColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="8b352-102">SortColumn property (RDS)</span></span>

<span data-ttu-id="8b352-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b352-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b352-104">Indica por qual coluna os registros serão classificados.</span><span class="sxs-lookup"><span data-stu-id="8b352-104">Indicates by which column to sort the records.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b352-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b352-105">Syntax</span></span>

<span data-ttu-id="8b352-106">*DataControl*. SortColumn = *String*</span><span class="sxs-lookup"><span data-stu-id="8b352-106">*DataControl*.SortColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="8b352-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b352-107">Parameters</span></span>

|<span data-ttu-id="8b352-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b352-108">Parameter</span></span>|<span data-ttu-id="8b352-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b352-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8b352-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="8b352-110">*DataControl*</span></span> |<span data-ttu-id="8b352-111">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="8b352-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="8b352-112">*String*</span><span class="sxs-lookup"><span data-stu-id="8b352-112">*String*</span></span> |<span data-ttu-id="8b352-113">Um valor **String** que representa o nome ou o alias da coluna pela qual os registros serão classificados.</span><span class="sxs-lookup"><span data-stu-id="8b352-113">A **String** value that represents the name or alias of the column by which to sort the records.</span></span>|

## <a name="remarks"></a><span data-ttu-id="8b352-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b352-114">Remarks</span></span>

<span data-ttu-id="8b352-p101">As propriedades **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e filtragem no cache do lado do cliente. A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna. A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache. O método [Reset](reset-method-rds.md) executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="8b352-p101">The **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="8b352-119">Para classificar em um **Recordset**, você deverá primeiramente salvar quaisquer alterações pendentes.</span><span class="sxs-lookup"><span data-stu-id="8b352-119">To sort on a **Recordset**, you must first save any pending changes.</span></span> <span data-ttu-id="8b352-120">Se você estiver utilizando o **RDS.DataControl**, será possível utilizar o método [SubmitChanges](submitchanges-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="8b352-120">If you are using the **RDS.DataControl**, you can use the [SubmitChanges](submitchanges-method-rds.md) method.</span></span> <span data-ttu-id="8b352-121">Por exemplo, se sua **RDS. DataControl** é denominado ADC1, seu código seria ADC1. SubmitChanges.</span><span class="sxs-lookup"><span data-stu-id="8b352-121">For example, if your **RDS.DataControl** is named ADC1, your code would be ADC1.SubmitChanges .</span></span> <span data-ttu-id="8b352-122">Se estiver utilizando um **Recordset** do ADO, você poderá utilizar seu método [UpdateBatch](updatebatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8b352-122">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="8b352-123">O uso do **UpdateBatch** é o método recomendado para os objetos **Recordset** criados com o método [CreateRecordset](createrecordset-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="8b352-123">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="8b352-124">Por exemplo, seu código poderia ser myRS.UpdateBatch ou.</span><span class="sxs-lookup"><span data-stu-id="8b352-124">For example, your code could be myRS.UpdateBatch or .</span></span> <span data-ttu-id="8b352-125">Se estiver utilizando um **Recordset** do ADO, você poderá utilizar seu método [UpdateBatch](updatebatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8b352-125">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="8b352-126">O uso do **UpdateBatch** é o método recomendado para os objetos **Recordset** criados com o método [CreateRecordset](createrecordset-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="8b352-126">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="8b352-127">Por exemplo, seu código poderia ser myRS.UpdateBatch ou ADC1. Recordset.UpdateBatch.</span><span class="sxs-lookup"><span data-stu-id="8b352-127">For example, your code could be myRS.UpdateBatch or ADC1.Recordset.UpdateBatch .</span></span>


---
title: Propriedade SortColumn (RDS)
TOCTitle: SortColumn property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bccd0eb536ec67937e8c3659b2ac62ef49a0bb3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924061"
---
# <a name="sortcolumn-property-rds"></a><span data-ttu-id="9d173-102">Propriedade SortColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="9d173-102">SortColumn property (RDS)</span></span>


<span data-ttu-id="9d173-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d173-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9d173-104">Indica por qual coluna os registros serão classificados.</span><span class="sxs-lookup"><span data-stu-id="9d173-104">Indicates by which column to sort the records.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d173-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d173-105">Syntax</span></span>

<span data-ttu-id="9d173-106">*DataControl*. SortColumn = *String*</span><span class="sxs-lookup"><span data-stu-id="9d173-106">*DataControl*.SortColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="9d173-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d173-107">Parameters</span></span>

  - <span data-ttu-id="9d173-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="9d173-108">*DataControl*</span></span>

  - <span data-ttu-id="9d173-109">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="9d173-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="9d173-110">*String*</span><span class="sxs-lookup"><span data-stu-id="9d173-110">*String*</span></span>

  - <span data-ttu-id="9d173-111">Um valor **String** que representa o nome ou o alias da coluna pela qual os registros serão classificados.</span><span class="sxs-lookup"><span data-stu-id="9d173-111">A **String** value that represents the name or alias of the column by which to sort the records.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d173-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d173-112">Remarks</span></span>

<span data-ttu-id="9d173-p101">As propriedades **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e filtragem no cache do lado do cliente. A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna. A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache. O método [Reset](reset-method-rds.md) executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="9d173-p101">The **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="9d173-117">Para classificar em um **Recordset**, você deverá primeiramente salvar quaisquer alterações pendentes.</span><span class="sxs-lookup"><span data-stu-id="9d173-117">To sort on a **Recordset**, you must first save any pending changes.</span></span> <span data-ttu-id="9d173-118">Se você estiver utilizando o **RDS.DataControl**, será possível utilizar o método [SubmitChanges](submitchanges-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="9d173-118">If you are using the **RDS.DataControl**, you can use the [SubmitChanges](submitchanges-method-rds.md) method.</span></span> <span data-ttu-id="9d173-119">Por exemplo, se sua **RDS. DataControl** é denominado ADC1, seu código seria ADC1. SubmitChanges.</span><span class="sxs-lookup"><span data-stu-id="9d173-119">For example, if your **RDS.DataControl** is named ADC1, your code would be ADC1.SubmitChanges .</span></span> <span data-ttu-id="9d173-120">Se estiver utilizando um **Recordset** do ADO, você poderá utilizar seu método [UpdateBatch](updatebatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9d173-120">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="9d173-121">O uso do **UpdateBatch** é o método recomendado para os objetos **Recordset** criados com o método [CreateRecordset](createrecordset-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="9d173-121">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="9d173-122">Por exemplo, seu código poderia ser myRS.UpdateBatch ou.</span><span class="sxs-lookup"><span data-stu-id="9d173-122">For example, your code could be myRS.UpdateBatch or .</span></span> <span data-ttu-id="9d173-123">Se estiver utilizando um **Recordset** do ADO, você poderá utilizar seu método [UpdateBatch](updatebatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9d173-123">If you are using an ADO **Recordset**, you can use its [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="9d173-124">O uso do **UpdateBatch** é o método recomendado para os objetos **Recordset** criados com o método [CreateRecordset](createrecordset-method-rds.md).</span><span class="sxs-lookup"><span data-stu-id="9d173-124">Using **UpdateBatch** is the recommended method for **Recordset** objects created with the [CreateRecordset](createrecordset-method-rds.md) method.</span></span> <span data-ttu-id="9d173-125">Por exemplo, seu código poderia ser myRS.UpdateBatch ou ADC1. Recordset.UpdateBatch.</span><span class="sxs-lookup"><span data-stu-id="9d173-125">For example, your code could be myRS.UpdateBatch or ADC1.Recordset.UpdateBatch .</span></span>


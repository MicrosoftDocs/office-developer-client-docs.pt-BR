---
title: Propriedade Rowset (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: be2a4855b3411a11ddd5a76225acaa52344877a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306738"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="b335e-102">Propriedade Rowset (ADO)</span><span class="sxs-lookup"><span data-stu-id="b335e-102">Rowset property (ADO)</span></span>

<span data-ttu-id="b335e-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b335e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b335e-104">Obtém ou define um objeto **Rowset** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="b335e-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="b335e-105">Quando você usa o\_conjunto de linhas, o conjunto de linhas é transformado em um objeto **Recordset** do ADO.</span><span class="sxs-lookup"><span data-stu-id="b335e-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="b335e-106">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b335e-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b335e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b335e-107">Syntax</span></span>

<span data-ttu-id="b335e-108">HRESULT get\_Rowset (\[out, retval\] IUnknown\* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="b335e-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="b335e-109">HRESULT colocar\_Rowset (\[em\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="b335e-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="b335e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b335e-110">Parameters</span></span>

|<span data-ttu-id="b335e-111">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="b335e-111">Parameter</span></span>|<span data-ttu-id="b335e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b335e-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b335e-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="b335e-113">*ppRowset*</span></span> |<span data-ttu-id="b335e-114">Ponteiro para um objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="b335e-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="b335e-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="b335e-115">*PRowset*</span></span> |<span data-ttu-id="b335e-116">Um objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="b335e-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="b335e-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b335e-117">Return values</span></span>

<span data-ttu-id="b335e-118">Este método de propriedade retorna os valores HRESULT padrão, incluindo\_S OK E\_o e falha.</span><span class="sxs-lookup"><span data-stu-id="b335e-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b335e-119">Aplicável a</span><span class="sxs-lookup"><span data-stu-id="b335e-119">Applies to</span></span>

[<span data-ttu-id="b335e-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="b335e-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


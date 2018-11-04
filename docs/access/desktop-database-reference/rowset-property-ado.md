---
title: Propriedade Rowset (ADO)
TOCTitle: Rowset property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0d5979cb42e2ed4a979dc07016a4bb02b8097994
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949786"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="4233c-102">Propriedade Rowset (ADO)</span><span class="sxs-lookup"><span data-stu-id="4233c-102">Rowset property (ADO)</span></span>

<span data-ttu-id="4233c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4233c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4233c-104">Obtém ou define um objeto **Rowset** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="4233c-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="4233c-105">Quando você usa put\_Rowset, o conjunto de linhas seja transformado em um objeto **Recordset** do ADO.</span><span class="sxs-lookup"><span data-stu-id="4233c-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="4233c-106">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4233c-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4233c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4233c-107">Syntax</span></span>

<span data-ttu-id="4233c-108">Get HRESULT\_Rowset (\[check-out, retval\] IUnknown\* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="4233c-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="4233c-109">Colocar HRESULT\_Rowset (\[na\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="4233c-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="4233c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4233c-110">Parameters</span></span>

|<span data-ttu-id="4233c-111">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="4233c-111">Parameter</span></span>|<span data-ttu-id="4233c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="4233c-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4233c-113">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="4233c-113">*ppRowset*</span></span> |<span data-ttu-id="4233c-114">Ponteiro para um objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4233c-114">Pointer to an OLE DB **Rowset** object.</span></span>|
|<span data-ttu-id="4233c-115">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="4233c-115">*PRowset*</span></span> |<span data-ttu-id="4233c-116">Um objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4233c-116">An OLE DB **Rowset** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="4233c-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4233c-117">Return values</span></span>

<span data-ttu-id="4233c-118">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="4233c-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="4233c-119">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="4233c-119">Applies to</span></span>

[<span data-ttu-id="4233c-120">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="4233c-120">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


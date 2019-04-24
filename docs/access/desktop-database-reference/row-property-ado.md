---
title: Propriedade Row-ActiveX Data Objects (ADO)
TOCTitle: Row property (ADO)
ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15)
ms:contentKeyID: 48543562
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4beaa742bfc46ecd32fc04733c3e6ddaf12aa2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306479"
---
# <a name="row-property-ado"></a><span data-ttu-id="66ae3-102">Propriedade Row (ADO)</span><span class="sxs-lookup"><span data-stu-id="66ae3-102">Row property (ADO)</span></span>

<span data-ttu-id="66ae3-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66ae3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66ae3-104">Obtém ou define um objeto **Row** do OLE DB a partir de/em um objeto **ADORecordConstruction**.</span><span class="sxs-lookup"><span data-stu-id="66ae3-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="66ae3-105">Quando você usa **colocar\_linha** para definir um objeto **Row** , uma linha é TransformaDA em um objeto **Record** do ADO.</span><span class="sxs-lookup"><span data-stu-id="66ae3-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="66ae3-106">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="66ae3-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ae3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66ae3-107">Syntax</span></span>

<span data-ttu-id="66ae3-108">HRESULT obter\_linha (\[out, retval\] IUnknown\* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="66ae3-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="66ae3-109">Linha HRESULT\_put (\[em\] IUnknown\* Prow);</span><span class="sxs-lookup"><span data-stu-id="66ae3-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="66ae3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66ae3-110">Parameters</span></span>

|<span data-ttu-id="66ae3-111">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="66ae3-111">Parameter</span></span>|<span data-ttu-id="66ae3-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="66ae3-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="66ae3-113">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="66ae3-113">*ppRow*</span></span> |<span data-ttu-id="66ae3-114">Ponteiro para um objeto **Row** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="66ae3-114">Pointer to an OLE DB **Row** object.</span></span>|
|<span data-ttu-id="66ae3-115">*PRow*</span><span class="sxs-lookup"><span data-stu-id="66ae3-115">*PRow*</span></span> |<span data-ttu-id="66ae3-116">Um objeto **Row** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="66ae3-116">An OLE DB **Row** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="66ae3-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="66ae3-117">Return values</span></span>

<span data-ttu-id="66ae3-118">Este método de propriedade retorna os valores HRESULT padrão, incluindo\_S OK E\_o e falha.</span><span class="sxs-lookup"><span data-stu-id="66ae3-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="66ae3-119">Aplicável a</span><span class="sxs-lookup"><span data-stu-id="66ae3-119">Applies to</span></span>

[<span data-ttu-id="66ae3-120">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="66ae3-120">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)


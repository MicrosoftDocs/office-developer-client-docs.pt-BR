---
title: Propriedade Row - ActiveX Data Objects (ADO)
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
# <a name="row-property-ado"></a><span data-ttu-id="17b9d-102">Propriedade Row (ADO)</span><span class="sxs-lookup"><span data-stu-id="17b9d-102">Row property (ADO)</span></span>

<span data-ttu-id="17b9d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="17b9d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="17b9d-104">Obtém ou define um objeto **Row** do OLE DB a partir de/em um objeto **ADORecordConstruction**.</span><span class="sxs-lookup"><span data-stu-id="17b9d-104">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="17b9d-105">Quando você usa **colocar \_ Row** para definir **um objeto Row,** uma linha é transformada em um objeto **Record** do ADO.</span><span class="sxs-lookup"><span data-stu-id="17b9d-105">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="17b9d-106">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="17b9d-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b9d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17b9d-107">Syntax</span></span>

<span data-ttu-id="17b9d-108">HRESULT get \_ Row( \[ out, retval \] IUnknown \* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="17b9d-108">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="17b9d-109">HRESULT put \_ Row( \[ in \] IUnknown \* pRow);</span><span class="sxs-lookup"><span data-stu-id="17b9d-109">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="17b9d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17b9d-110">Parameters</span></span>

|<span data-ttu-id="17b9d-111">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="17b9d-111">Parameter</span></span>|<span data-ttu-id="17b9d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="17b9d-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="17b9d-113">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="17b9d-113">*ppRow*</span></span> |<span data-ttu-id="17b9d-114">Ponteiro para um objeto **Row** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="17b9d-114">Pointer to an OLE DB **Row** object.</span></span>|
|<span data-ttu-id="17b9d-115">*PRow*</span><span class="sxs-lookup"><span data-stu-id="17b9d-115">*PRow*</span></span> |<span data-ttu-id="17b9d-116">Um objeto **Row** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="17b9d-116">An OLE DB **Row** object.</span></span>|

## <a name="return-values"></a><span data-ttu-id="17b9d-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="17b9d-117">Return values</span></span>

<span data-ttu-id="17b9d-118">Esse método de propriedade retorna os valores HRESULT padrão, incluindo S \_ OK e E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="17b9d-118">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="17b9d-119">Aplicável a</span><span class="sxs-lookup"><span data-stu-id="17b9d-119">Applies to</span></span>

[<span data-ttu-id="17b9d-120">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="17b9d-120">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)


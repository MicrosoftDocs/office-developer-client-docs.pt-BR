---
title: Propriedade Chapter (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d7523a930feed7431bf8be0bbb7222a4b305483
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949394"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="561f5-102">Propriedade Chapter (ADO)</span><span class="sxs-lookup"><span data-stu-id="561f5-102">Chapter property (ADO)</span></span>

<span data-ttu-id="561f5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="561f5-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="561f5-104">Obtém ou configura um objeto **Chapter** do OLE DB de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="561f5-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="561f5-105">Quando você usa **colocar\_capítulo** para definir o objeto de **capítulo** , um subconjunto de linhas seja transformado em um objeto **Recordset** do ADO.</span><span class="sxs-lookup"><span data-stu-id="561f5-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="561f5-106">Isso define o capítulo atual do objeto **Rowset**.</span><span class="sxs-lookup"><span data-stu-id="561f5-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="561f5-107">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="561f5-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="561f5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="561f5-108">Syntax</span></span>

<span data-ttu-id="561f5-109">Get HRESULT\_capítulo (\[check-out, retval\] longo\* plChapter);</span><span class="sxs-lookup"><span data-stu-id="561f5-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="561f5-110">Colocar HRESULT\_capítulo (\[na\] lChapter longo);</span><span class="sxs-lookup"><span data-stu-id="561f5-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="561f5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="561f5-111">Parameters</span></span>

|<span data-ttu-id="561f5-112">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="561f5-112">Parameter</span></span>|<span data-ttu-id="561f5-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="561f5-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="561f5-114">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="561f5-114">*plChapter*</span></span> |<span data-ttu-id="561f5-115">Ponteiro para o identificador de um capítulo.</span><span class="sxs-lookup"><span data-stu-id="561f5-115">Pointer to the handle of a chapter.</span></span>|
|<span data-ttu-id="561f5-116">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="561f5-116">*LChapter*</span></span> |<span data-ttu-id="561f5-117">Identificador de um capítulo.</span><span class="sxs-lookup"><span data-stu-id="561f5-117">Handle of a chapter.</span></span>|

## <a name="return-values"></a><span data-ttu-id="561f5-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="561f5-118">Return values</span></span>

<span data-ttu-id="561f5-119">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="561f5-119">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="561f5-120">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="561f5-120">Applies To</span></span>

[<span data-ttu-id="561f5-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="561f5-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


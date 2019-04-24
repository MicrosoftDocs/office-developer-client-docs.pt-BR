---
title: Propriedade Chapter (ADO)
TOCTitle: Chapter property (ADO)
ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15)
ms:contentKeyID: 48548014
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4f4efc2ffab9f7996b2d805658b985badbaf87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296392"
---
# <a name="chapter-property-ado"></a><span data-ttu-id="5f9a1-102">Propriedade Chapter (ADO)</span><span class="sxs-lookup"><span data-stu-id="5f9a1-102">Chapter property (ADO)</span></span>

<span data-ttu-id="5f9a1-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f9a1-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="5f9a1-104">Obtém ou configura um objeto **Chapter** do OLE DB de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="5f9a1-104">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="5f9a1-105">Quando você usa **o\_Chapter** para definir o objeto **Chapter** , um subconjunto de linhas é transformado em um objeto **Recordset** do ADO.</span><span class="sxs-lookup"><span data-stu-id="5f9a1-105">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="5f9a1-106">Isso define o capítulo atual do objeto **Rowset**.</span><span class="sxs-lookup"><span data-stu-id="5f9a1-106">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="5f9a1-107">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5f9a1-107">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f9a1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f9a1-108">Syntax</span></span>

<span data-ttu-id="5f9a1-109">HRESULT obter\_capítulo (\[out, retval\] Long\* plChapter);</span><span class="sxs-lookup"><span data-stu-id="5f9a1-109">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="5f9a1-110">Módulo HRESULT\_put (\[em\] Long lChapter);</span><span class="sxs-lookup"><span data-stu-id="5f9a1-110">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="5f9a1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f9a1-111">Parameters</span></span>

|<span data-ttu-id="5f9a1-112">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f9a1-112">Parameter</span></span>|<span data-ttu-id="5f9a1-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f9a1-113">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5f9a1-114">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="5f9a1-114">*plChapter*</span></span> |<span data-ttu-id="5f9a1-115">Ponteiro para o identificador de um capítulo.</span><span class="sxs-lookup"><span data-stu-id="5f9a1-115">Pointer to the handle of a chapter.</span></span>|
|<span data-ttu-id="5f9a1-116">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="5f9a1-116">*LChapter*</span></span> |<span data-ttu-id="5f9a1-117">Identificador de um capítulo.</span><span class="sxs-lookup"><span data-stu-id="5f9a1-117">Handle of a chapter.</span></span>|

## <a name="return-values"></a><span data-ttu-id="5f9a1-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5f9a1-118">Return values</span></span>

<span data-ttu-id="5f9a1-119">Este método de propriedade retorna os valores HRESULT padrão, incluindo\_S OK E\_o e falha.</span><span class="sxs-lookup"><span data-stu-id="5f9a1-119">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="5f9a1-120">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="5f9a1-120">Applies To</span></span>

[<span data-ttu-id="5f9a1-121">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="5f9a1-121">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)


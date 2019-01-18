---
title: Propriedade ParentRow (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2844f7c93164c4b384a895cd32a13bd682154ce3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721721"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="35713-102">Propriedade ParentRow (ADO)</span><span class="sxs-lookup"><span data-stu-id="35713-102">ParentRow property (ADO)</span></span>

<span data-ttu-id="35713-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="35713-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="35713-104">Define o contêiner de um objeto **Row** do OLE DB em um objeto **ADORecordConstruction**, de forma que o pai da linha seja transformado em um objeto **Record** do ADO.</span><span class="sxs-lookup"><span data-stu-id="35713-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="35713-105">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="35713-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="35713-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35713-106">Syntax</span></span>

<span data-ttu-id="35713-107">Colocar HRESULT\_ParentRow (\[na\] IUnknown\* pParent);</span><span class="sxs-lookup"><span data-stu-id="35713-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="35713-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35713-108">Parameters</span></span>

|<span data-ttu-id="35713-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="35713-109">Parameter</span></span>|<span data-ttu-id="35713-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="35713-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="35713-111">*pParent*</span><span class="sxs-lookup"><span data-stu-id="35713-111">*pParent*</span></span> |<span data-ttu-id="35713-112">O contêiner de uma linha.</span><span class="sxs-lookup"><span data-stu-id="35713-112">A container of a row.</span></span>|

## <a name="return-values"></a><span data-ttu-id="35713-113">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="35713-113">Return values</span></span>

<span data-ttu-id="35713-114">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="35713-114">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="35713-115">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="35713-115">Applies to</span></span>

[<span data-ttu-id="35713-116">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="35713-116">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)


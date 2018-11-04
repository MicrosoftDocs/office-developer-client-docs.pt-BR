---
title: Propriedade ParentRow (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06bb1110dfa7e7a055fa6cd863dcd2cc17f3f585
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950143"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="f9279-102">Propriedade ParentRow (ADO)</span><span class="sxs-lookup"><span data-stu-id="f9279-102">ParentRow property (ADO)</span></span>

<span data-ttu-id="f9279-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9279-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9279-104">Define o contêiner de um objeto **Row** do OLE DB em um objeto **ADORecordConstruction**, de forma que o pai da linha seja transformado em um objeto **Record** do ADO.</span><span class="sxs-lookup"><span data-stu-id="f9279-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="f9279-105">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="f9279-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9279-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9279-106">Syntax</span></span>

<span data-ttu-id="f9279-107">Colocar HRESULT\_ParentRow (\[na\] IUnknown\* pParent);</span><span class="sxs-lookup"><span data-stu-id="f9279-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="f9279-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9279-108">Parameters</span></span>

|<span data-ttu-id="f9279-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9279-109">Parameter</span></span>|<span data-ttu-id="f9279-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9279-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f9279-111">*pParent*</span><span class="sxs-lookup"><span data-stu-id="f9279-111">*pParent*</span></span> |<span data-ttu-id="f9279-112">O contêiner de uma linha.</span><span class="sxs-lookup"><span data-stu-id="f9279-112">A container of a row.</span></span>|

## <a name="return-values"></a><span data-ttu-id="f9279-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f9279-113">Return values</span></span>

<span data-ttu-id="f9279-114">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="f9279-114">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f9279-115">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="f9279-115">Applies to</span></span>

[<span data-ttu-id="f9279-116">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="f9279-116">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)


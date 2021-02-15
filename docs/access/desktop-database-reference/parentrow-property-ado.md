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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287735"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="9efec-102">Propriedade ParentRow (ADO)</span><span class="sxs-lookup"><span data-stu-id="9efec-102">ParentRow property (ADO)</span></span>

<span data-ttu-id="9efec-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9efec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9efec-104">Define o contêiner de um objeto **Row** do OLE DB em um objeto **ADORecordConstruction**, de forma que o pai da linha seja transformado em um objeto **Record** do ADO.</span><span class="sxs-lookup"><span data-stu-id="9efec-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="9efec-105">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="9efec-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9efec-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9efec-106">Syntax</span></span>

<span data-ttu-id="9efec-107">HRESULT put \_ ParentRow( \[ in \] IUnknown \* pParent);</span><span class="sxs-lookup"><span data-stu-id="9efec-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="9efec-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9efec-108">Parameters</span></span>

|<span data-ttu-id="9efec-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="9efec-109">Parameter</span></span>|<span data-ttu-id="9efec-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9efec-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="9efec-111">*pParent*</span><span class="sxs-lookup"><span data-stu-id="9efec-111">*pParent*</span></span> |<span data-ttu-id="9efec-112">O contêiner de uma linha.</span><span class="sxs-lookup"><span data-stu-id="9efec-112">A container of a row.</span></span>|

## <a name="return-values"></a><span data-ttu-id="9efec-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9efec-113">Return values</span></span>

<span data-ttu-id="9efec-114">Esse método de propriedade retorna os valores HRESULT padrão, incluindo S \_ OK e E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="9efec-114">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9efec-115">Aplicável a</span><span class="sxs-lookup"><span data-stu-id="9efec-115">Applies to</span></span>

[<span data-ttu-id="9efec-116">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="9efec-116">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)


---
title: Propriedade ParentRow (ADO)
TOCTitle: ParentRow Property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 834dcaed7d1acdcf66410584436e2ccee8c91c56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465443"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="42e0f-102">Propriedade ParentRow (ADO)</span><span class="sxs-lookup"><span data-stu-id="42e0f-102">ParentRow Property (ADO)</span></span>


<span data-ttu-id="42e0f-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="42e0f-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="42e0f-104">Define o contêiner de um objeto **Row** do OLE DB em um objeto **ADORecordConstruction**, de forma que o pai da linha seja transformado em um objeto **Record** do ADO.</span><span class="sxs-lookup"><span data-stu-id="42e0f-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="42e0f-105">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="42e0f-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="42e0f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42e0f-106">Syntax</span></span>

<span data-ttu-id="42e0f-107">Colocar HRESULT\_ParentRow (\[na\] IUnknown\* pParent);</span><span class="sxs-lookup"><span data-stu-id="42e0f-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="42e0f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42e0f-108">Parameters</span></span>

  - <span data-ttu-id="42e0f-109">*pParent*</span><span class="sxs-lookup"><span data-stu-id="42e0f-109">*pParent*</span></span>

  - <span data-ttu-id="42e0f-110">O contêiner de uma linha.</span><span class="sxs-lookup"><span data-stu-id="42e0f-110">A container of a row.</span></span>

## <a name="return-values"></a><span data-ttu-id="42e0f-111">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="42e0f-111">Return Values</span></span>

<span data-ttu-id="42e0f-112">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="42e0f-112">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="42e0f-113">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="42e0f-113">Applies To</span></span>

[<span data-ttu-id="42e0f-114">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="42e0f-114">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)


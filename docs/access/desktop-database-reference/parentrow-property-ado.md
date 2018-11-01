---
title: Propriedade ParentRow (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28f0d1c7dbc0e062ff133b9f9997f1a737c3262e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872127"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="9cefd-102">Propriedade ParentRow (ADO)</span><span class="sxs-lookup"><span data-stu-id="9cefd-102">ParentRow property (ADO)</span></span>


<span data-ttu-id="9cefd-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9cefd-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="9cefd-104">Define o contêiner de um objeto **Row** do OLE DB em um objeto **ADORecordConstruction**, de forma que o pai da linha seja transformado em um objeto **Record** do ADO.</span><span class="sxs-lookup"><span data-stu-id="9cefd-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="9cefd-105">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="9cefd-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cefd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cefd-106">Syntax</span></span>

<span data-ttu-id="9cefd-107">Colocar HRESULT\_ParentRow (\[na\] IUnknown\* pParent);</span><span class="sxs-lookup"><span data-stu-id="9cefd-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="9cefd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cefd-108">Parameters</span></span>

  - <span data-ttu-id="9cefd-109">*pParent*</span><span class="sxs-lookup"><span data-stu-id="9cefd-109">*pParent*</span></span>

  - <span data-ttu-id="9cefd-110">O contêiner de uma linha.</span><span class="sxs-lookup"><span data-stu-id="9cefd-110">A container of a row.</span></span>

## <a name="return-values"></a><span data-ttu-id="9cefd-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9cefd-111">Return values</span></span>

<span data-ttu-id="9cefd-112">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="9cefd-112">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9cefd-113">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="9cefd-113">Applies To</span></span>

[<span data-ttu-id="9cefd-114">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="9cefd-114">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)


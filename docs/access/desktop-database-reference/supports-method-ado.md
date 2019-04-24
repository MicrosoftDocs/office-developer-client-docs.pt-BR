---
title: Método Supports (ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42447614c5fc58bc4eb2933354908693adf68ce6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308460"
---
# <a name="supports-method-ado"></a><span data-ttu-id="07cfd-102">Método Supports (ADO)</span><span class="sxs-lookup"><span data-stu-id="07cfd-102">Supports method (ADO)</span></span>

<span data-ttu-id="07cfd-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="07cfd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="07cfd-104">Determina se um objeto [Recordset](recordset-object-ado.md) especificado suporta um tipo de funcionalidade específico.</span><span class="sxs-lookup"><span data-stu-id="07cfd-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="07cfd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07cfd-105">Syntax</span></span>

<span data-ttu-id="07cfd-106">\*\* = *Recordset*Boolean. Suporte (*CursorOptions*)</span><span class="sxs-lookup"><span data-stu-id="07cfd-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

## <a name="return-value"></a><span data-ttu-id="07cfd-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="07cfd-107">Return value</span></span>

<span data-ttu-id="07cfd-108">Retorna um valor **Boolean** que indica se todos os recursos identificados pelo argumento *CursorOptions* são suportados pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="07cfd-108">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="07cfd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07cfd-109">Parameters</span></span>

|<span data-ttu-id="07cfd-110">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="07cfd-110">Parameter</span></span>|<span data-ttu-id="07cfd-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="07cfd-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="07cfd-112">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="07cfd-112">*CursorOptions*</span></span> |<span data-ttu-id="07cfd-113">Uma expressão **Long** que consiste em um ou mais valores [CursorOptionEnum](cursoroptionenum.md).</span><span class="sxs-lookup"><span data-stu-id="07cfd-113">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>|

## <a name="remarks"></a><span data-ttu-id="07cfd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="07cfd-114">Remarks</span></span>

<span data-ttu-id="07cfd-p101">Utilize o método **Supports** para determinar quais tipos de funcionalidade um objeto **Recordset** suporta. Se o objeto **Recordset** suportar os recursos cujas constantes correspondentes estão em *CursorOptions*, o método **Supports** retornará **True**. Caso contrário, ele retornará **False**.</span><span class="sxs-lookup"><span data-stu-id="07cfd-p101">Use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <span data-ttu-id="07cfd-p102">[!OBSERVAçãO] Embora o método **Supports** possa retornar **True** para uma determinada funcionalidade, isso não garante que o provedor possa tornar o recurso disponível sob todas as circunstâncias. O método **Supports** simplesmente retorna se o provedor pode suportar a funcionalidade especificada, supondo que determinadas condições sejam atendidas. Por exemplo, o método **Supports** pode indicar que um objeto **Recordset** suporta atualizações, muito embora o cursor tenha como base uma junção de várias tabelas, algumas colunas das quais não são atualizáveis.</span><span class="sxs-lookup"><span data-stu-id="07cfd-p102">Although the **Supports** method may return **True** for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The **Supports** method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the **Supports** method may indicate that a **Recordset** object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span>



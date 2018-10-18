---
title: Método Supports (ADO)
TOCTitle: Supports Method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ceeab22cda05738fdcec090acb5b4a2d6fc88a5b
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604257"
---
# <a name="supports-method-ado"></a><span data-ttu-id="fb6ea-102">Método Supports (ADO)</span><span class="sxs-lookup"><span data-stu-id="fb6ea-102">Supports Method (ADO)</span></span>


<span data-ttu-id="fb6ea-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb6ea-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fb6ea-104">Determina se um objeto [Recordset](recordset-object-ado.md) especificado suporta um tipo de funcionalidade específico.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6ea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb6ea-105">Syntax</span></span>

<span data-ttu-id="fb6ea-106">*Boolean* = *recordset*. Suporta (*CursorOptions*)</span><span class="sxs-lookup"><span data-stu-id="fb6ea-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

<span data-ttu-id="fb6ea-107"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="fb6ea-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="fb6ea-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fb6ea-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="fb6ea-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fb6ea-109">Return value</span></span>
>>>>>>> <span data-ttu-id="fb6ea-110">mestre</span><span class="sxs-lookup"><span data-stu-id="fb6ea-110">master</span></span>

<span data-ttu-id="fb6ea-111">Retorna um valor **Boolean** que indica se todos os recursos identificados pelo argumento *CursorOptions* são suportados pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-111">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb6ea-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb6ea-112">Parameters</span></span>

  - <span data-ttu-id="fb6ea-113">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="fb6ea-113">*CursorOptions*</span></span>

  - <span data-ttu-id="fb6ea-114">Uma expressão **Long** que consiste em um ou mais valores [CursorOptionEnum](cursoroptionenum.md).</span><span class="sxs-lookup"><span data-stu-id="fb6ea-114">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb6ea-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb6ea-115">Remarks</span></span>

<span data-ttu-id="fb6ea-p101">Utilize o método **Supports** para determinar quais tipos de funcionalidade um objeto **Recordset** suporta. Se o objeto **Recordset** suportar os recursos cujas constantes correspondentes estão em *CursorOptions*, o método **Supports** retornará **True**. Caso contrário, ele retornará **False**.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-p101">Use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fb6ea-p102">[!OBSERVAçãO] Embora o método <STRONG>Supports</STRONG> possa retornar <STRONG>True</STRONG> para uma determinada funcionalidade, isso não garante que o provedor possa tornar o recurso disponível sob todas as circunstâncias. O método <STRONG>Supports</STRONG> simplesmente retorna se o provedor pode suportar a funcionalidade especificada, supondo que determinadas condições sejam atendidas. Por exemplo, o método <STRONG>Supports</STRONG> pode indicar que um objeto <STRONG>Recordset</STRONG> suporta atualizações, muito embora o cursor tenha como base uma junção de várias tabelas, algumas colunas das quais não são atualizáveis.</span><span class="sxs-lookup"><span data-stu-id="fb6ea-p102">Although the <STRONG>Supports</STRONG> method may return <STRONG>True</STRONG> for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The <STRONG>Supports</STRONG> method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the <STRONG>Supports</STRONG> method may indicate that a <STRONG>Recordset</STRONG> object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span></P>



---
title: Método Supports (ADO)
TOCTitle: Supports Method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 61e6a4f3a5771c4d223380160204e4b0b350f210
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461987"
---
# <a name="supports-method-ado"></a><span data-ttu-id="59881-102">Método Supports (ADO)</span><span class="sxs-lookup"><span data-stu-id="59881-102">Supports Method (ADO)</span></span>


<span data-ttu-id="59881-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="59881-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="59881-104">Determina se um objeto [Recordset](recordset-object-ado.md) especificado suporta um tipo de funcionalidade específico.</span><span class="sxs-lookup"><span data-stu-id="59881-104">Determines whether a specified [Recordset](recordset-object-ado.md) object supports a particular type of functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="59881-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59881-105">Syntax</span></span>

<span data-ttu-id="59881-106">*Boolean* = *recordset*. Suporta (*CursorOptions*)</span><span class="sxs-lookup"><span data-stu-id="59881-106">*boolean* = *recordset*.Supports (*CursorOptions*)</span></span>

## <a name="return-value"></a><span data-ttu-id="59881-107">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="59881-107">Return Value</span></span>

<span data-ttu-id="59881-108">Retorna um valor **Boolean** que indica se todos os recursos identificados pelo argumento *CursorOptions* são suportados pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="59881-108">Returns a **Boolean** value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider.</span></span>

## <a name="parameters"></a><span data-ttu-id="59881-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59881-109">Parameters</span></span>

  - <span data-ttu-id="59881-110">*CursorOptions*</span><span class="sxs-lookup"><span data-stu-id="59881-110">*CursorOptions*</span></span>

  - <span data-ttu-id="59881-111">Uma expressão **Long** que consiste em um ou mais valores [CursorOptionEnum](cursoroptionenum.md).</span><span class="sxs-lookup"><span data-stu-id="59881-111">A **Long** expression that consists of one or more [CursorOptionEnum](cursoroptionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="59881-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="59881-112">Remarks</span></span>

<span data-ttu-id="59881-p101">Utilize o método **Supports** para determinar quais tipos de funcionalidade um objeto **Recordset** suporta. Se o objeto **Recordset** suportar os recursos cujas constantes correspondentes estão em *CursorOptions*, o método **Supports** retornará **True**. Caso contrário, ele retornará **False**.</span><span class="sxs-lookup"><span data-stu-id="59881-p101">Use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="59881-p102">[!OBSERVAçãO] Embora o método <STRONG>Supports</STRONG> possa retornar <STRONG>True</STRONG> para uma determinada funcionalidade, isso não garante que o provedor possa tornar o recurso disponível sob todas as circunstâncias. O método <STRONG>Supports</STRONG> simplesmente retorna se o provedor pode suportar a funcionalidade especificada, supondo que determinadas condições sejam atendidas. Por exemplo, o método <STRONG>Supports</STRONG> pode indicar que um objeto <STRONG>Recordset</STRONG> suporta atualizações, muito embora o cursor tenha como base uma junção de várias tabelas, algumas colunas das quais não são atualizáveis.</span><span class="sxs-lookup"><span data-stu-id="59881-p102">Although the <STRONG>Supports</STRONG> method may return <STRONG>True</STRONG> for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The <STRONG>Supports</STRONG> method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the <STRONG>Supports</STRONG> method may indicate that a <STRONG>Recordset</STRONG> object supports updates even though the cursor is based on a multiple table join, some columns of which are not updatable.</span></span></P>



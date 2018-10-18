---
title: Método GetChildren (ADO)
TOCTitle: GetChildren Method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06474b6c4ecb29388367f8ceac7c7676002e1384
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602654"
---
# <a name="getchildren-method-ado"></a><span data-ttu-id="55254-102">Método GetChildren (ADO)</span><span class="sxs-lookup"><span data-stu-id="55254-102">GetChildren Method (ADO)</span></span>


<span data-ttu-id="55254-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="55254-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="55254-104">Retorna um [Recordset](recordset-object-ado.md) cujas linhas representam os filhos de uma coleção [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="55254-104">Returns a [Recordset](recordset-object-ado.md) whose rows represent the children of a collection [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="55254-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55254-105">Syntax</span></span>

<span data-ttu-id="55254-106">**Definir** *conjunto de registros*  =  *registro*. GetChildren</span><span class="sxs-lookup"><span data-stu-id="55254-106">**Set** *recordset* = *record*.GetChildren</span></span>

<span data-ttu-id="55254-107"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="55254-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="55254-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="55254-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="55254-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="55254-109">Return value</span></span>
>>>>>>> <span data-ttu-id="55254-110">mestre</span><span class="sxs-lookup"><span data-stu-id="55254-110">master</span></span>

<span data-ttu-id="55254-p101">Um objeto **Recordset** para o qual cada linha representa um filho do objeto **Record** atual. Por exemplo, os filhos de um **Record** que representa um diretório seriam os arquivos e subdiretórios contidos no diretório pai.</span><span class="sxs-lookup"><span data-stu-id="55254-p101">A **Recordset** object for which each row represents a child of the current **Record** object. For example, the children of a **Record** that represents a directory would be the files and subdirectories contained within the parent directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="55254-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="55254-113">Remarks</span></span>

<span data-ttu-id="55254-p102">O provedor determina quais colunas existem no **Recordset** retornado. Por exemplo, um provedor de fonte de documento sempre retorna um **Recordset** de recursos.</span><span class="sxs-lookup"><span data-stu-id="55254-p102">The provider determines what columns exist in the returned **Recordset**. For example, a document source provider always returns a resource **Recordset**.</span></span>


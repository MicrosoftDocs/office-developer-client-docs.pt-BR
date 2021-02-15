---
title: Método GetChildren (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ca8c113a377543ea8624972adb5958612a3fc72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292304"
---
# <a name="getchildren-method-ado"></a><span data-ttu-id="6b25a-102">Método GetChildren (ADO)</span><span class="sxs-lookup"><span data-stu-id="6b25a-102">GetChildren method (ADO)</span></span>


<span data-ttu-id="6b25a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b25a-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="6b25a-104">Retorna um [Recordset](recordset-object-ado.md) cujas linhas representam os filhos de uma coleção [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6b25a-104">Returns a [Recordset](recordset-object-ado.md) whose rows represent the children of a collection [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6b25a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b25a-105">Syntax</span></span>

<span data-ttu-id="6b25a-106">**Definir** *registro do conjunto de*  =  *registros.* GetChildren</span><span class="sxs-lookup"><span data-stu-id="6b25a-106">**Set** *recordset* = *record*.GetChildren</span></span>

## <a name="return-value"></a><span data-ttu-id="6b25a-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6b25a-107">Return value</span></span>

<span data-ttu-id="6b25a-p101">Um objeto **Recordset** para o qual cada linha representa um filho do objeto **Record** atual. Por exemplo, os filhos de um **Record** que representa um diretório seriam os arquivos e subdiretórios contidos no diretório pai.</span><span class="sxs-lookup"><span data-stu-id="6b25a-p101">A **Recordset** object for which each row represents a child of the current **Record** object. For example, the children of a **Record** that represents a directory would be the files and subdirectories contained within the parent directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b25a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b25a-110">Remarks</span></span>

<span data-ttu-id="6b25a-p102">O provedor determina quais colunas existem no **Recordset** retornado. Por exemplo, um provedor de fonte de documento sempre retorna um **Recordset** de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b25a-p102">The provider determines what columns exist in the returned **Recordset**. For example, a document source provider always returns a resource **Recordset**.</span></span>


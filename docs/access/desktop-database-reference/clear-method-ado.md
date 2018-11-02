---
title: Desmarque o método - ActiveX Data Objects (ADO)
TOCTitle: Clear method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 459ce19fab15e3e9bbd886a0f063005dab674fbc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929136"
---
# <a name="clear-method-ado"></a><span data-ttu-id="8c148-102">Método Clear (ADO)</span><span class="sxs-lookup"><span data-stu-id="8c148-102">Clear method (ADO)</span></span>


<span data-ttu-id="8c148-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c148-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c148-104">Remove todos os objetos **Error** da coleção **Errors**.</span><span class="sxs-lookup"><span data-stu-id="8c148-104">Removes all the **Error** objects from the **Errors** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c148-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c148-105">Syntax</span></span>

<span data-ttu-id="8c148-106">*Erros*. Limpar</span><span class="sxs-lookup"><span data-stu-id="8c148-106">*Errors*.Clear</span></span>

## <a name="remarks"></a><span data-ttu-id="8c148-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c148-107">Remarks</span></span>

<span data-ttu-id="8c148-p101">Utilize o método **Clear** na coleção [Errors](errors-collection-ado.md) para remover todos os objetos [Error](error-object-ado.md) existentes da coleção. Quando ocorre um erro, o ADO limpa automaticamente a coleção **Errors** e a preenche com objetos **Error** com base no novo erro.</span><span class="sxs-lookup"><span data-stu-id="8c148-p101">Use the **Clear** method on the [Errors](errors-collection-ado.md) collection to remove all existing [Error](error-object-ado.md) objects from the collection. When an error occurs, ADO automatically clears the **Errors** collection and fills it with **Error** objects based on the new error.</span></span>

<span data-ttu-id="8c148-p102">Algumas propriedades e métodos retornam avisos que aparecem como objetos **Error** na coleção **Errors** mas não suspendem a execução de um programa. Antes de chamar os métodos [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) em um objeto [Recordset](recordset-object-ado.md); o método [Open](open-method-ado-connection.md) em um objeto [Connection](connection-object-ado.md); ou definir a propriedade [Filter](filter-property-ado.md) em um objeto **Recordset**, chame o método **Clear** na coleção **Errors**. Dessa forma, é possível ler a propriedade [Count](count-property-ado.md) da coleção **Errors** para testar os avisos retornados.</span><span class="sxs-lookup"><span data-stu-id="8c148-p102">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution. Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object; the [Open](open-method-ado-connection.md) method on a [Connection](connection-object-ado.md) object; or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection. That way, you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>


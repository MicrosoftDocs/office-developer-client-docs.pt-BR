---
title: Feche o método - ActiveX Data Objects (ADO)
TOCTitle: Close Method (ADO)
ms:assetid: 26a7cced-ebeb-70be-f5de-96a35711bc37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249029(v=office.15)
ms:contentKeyID: 48543818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2df2f04f54242186093122bf70ef3365ad8617bf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875816"
---
# <a name="close-method-ado"></a><span data-ttu-id="8919e-102">Método Close (ADO)</span><span class="sxs-lookup"><span data-stu-id="8919e-102">Close Method (ADO)</span></span>


<span data-ttu-id="8919e-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8919e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8919e-104">Fecha um objeto aberto e quaisquer objetos dependentes.</span><span class="sxs-lookup"><span data-stu-id="8919e-104">Closes an open object and any dependent objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="8919e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8919e-105">Syntax</span></span>

<span data-ttu-id="8919e-106">*objeto*. Fechar</span><span class="sxs-lookup"><span data-stu-id="8919e-106">*object*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="8919e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8919e-107">Remarks</span></span>

<span data-ttu-id="8919e-108">Utilize o método **Close** para fechar um objeto [Connection](connection-object-ado.md), [Record](record-object-ado.md), [Recordset](recordset-object-ado.md) ou [Stream](stream-object-ado.md) e liberar quaisquer recursos associados do sistema.</span><span class="sxs-lookup"><span data-stu-id="8919e-108">Use the **Close** method to close a [Connection](connection-object-ado.md), a [Record](record-object-ado.md), a [Recordset](recordset-object-ado.md), or a [Stream](stream-object-ado.md) object to free any associated system resources.</span></span> <span data-ttu-id="8919e-109">O fechamento de um objeto não o remove da memória; é possível alterar as definições de propriedade e abri-lo novamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="8919e-109">Closing an object does not remove it from memory; you can change its property settings and open it again later.</span></span> <span data-ttu-id="8919e-110">Para eliminar completamente um objeto da memória, defina a variável de objeto para *Nothing* (no Visual Basic) após fechar o objeto.</span><span class="sxs-lookup"><span data-stu-id="8919e-110">To completely eliminate an object from memory, set the object variable to *Nothing* (in Visual Basic) after closing the object.</span></span>

<span data-ttu-id="8919e-111">**Connection**</span><span class="sxs-lookup"><span data-stu-id="8919e-111">**Connection**</span></span>

<span data-ttu-id="8919e-p102">A utilização do método **Close** para fechar um objeto **Connection** também fecha quaisquer objetos **Recordset** ativos associados à conexão. Um objeto [Command](command-object-ado.md) associado ao objeto **Connection** que está sendo fechado persistirá, mas não mais estará associado a um objeto **Connection**; isto é, sua propriedade [ActiveConnection](activeconnection-property-ado.md) será definida como **Nothing**. Além disso, a coleção **Parameters** do objeto [Command](parameters-collection-ado.md) será limpa de quaisquer parâmetros definidos pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="8919e-p102">Using the **Close** method to close a **Connection** object also closes any active **Recordset** objects associated with the connection. A [Command](command-object-ado.md) object associated with the **Connection** object you are closing will persist, but it will no longer be associated with a **Connection** object; that is, its [ActiveConnection](activeconnection-property-ado.md) property will be set to **Nothing**. Also, the **Command** object's [Parameters](parameters-collection-ado.md) collection will be cleared of any provider-defined parameters.</span></span>

<span data-ttu-id="8919e-p103">Posteriormente será possível chamar o método [Open](open-method-ado-connection.md) para restabelecer a conexão à mesma, ou outra, fonte de dados. Enquanto o objeto **Connection** está fechado, chamar quaisquer métodos que requeiram uma conexão aberta à fonte de dados gera um erro.</span><span class="sxs-lookup"><span data-stu-id="8919e-p103">You can later call the [Open](open-method-ado-connection.md) method to re-establish the connection to the same, or another, data source. While the **Connection** object is closed, calling any methods that require an open connection to the data source generates an error.</span></span>

<span data-ttu-id="8919e-p104">Fechar um objeto **Connection** enquanto existem objetos **Recordset** abertos na conexão reverte quaisquer alterações pendentes em todos os objetos **Recordset**. Fechar de forma explícita um objeto **Connection** (chamando o método **Close** ) enquanto uma transação está em andamento gera um erro. Se um objeto **Connection** ficar fora do escopo enquanto uma transação estiver em andamento, o ADO reverterá automaticamente a transação.</span><span class="sxs-lookup"><span data-stu-id="8919e-p104">Closing a **Connection** object while there are open **Recordset** objects on the connection rolls back any pending changes in all of the **Recordset** objects. Explicitly closing a **Connection** object (calling the **Close** method) while a transaction is in progress generates an error. If a **Connection** object falls out of scope while a transaction is in progress, ADO automatically rolls back the transaction.</span></span>

<span data-ttu-id="8919e-120">**Recordset, Record, Stream**</span><span class="sxs-lookup"><span data-stu-id="8919e-120">**Recordset, Record, Stream**</span></span>

<span data-ttu-id="8919e-p105">A utilização do método **Close** para fechar um objeto **Recordset**, **Record** ou **Stream** libera os dados associados e qualquer acesso exclusivo que possa ter existido aos dados por meio desse objeto específico. Posteriormente, é possível chamar o método [Open](open-method-ado-recordset.md) para reabrir o objeto com os mesmos atributos (ou modificados).</span><span class="sxs-lookup"><span data-stu-id="8919e-p105">Using the **Close** method to close a **Recordset**, **Record**, or **Stream** object releases the associated data and any exclusive access you may have had to the data through this particular object. You can later call the [Open](open-method-ado-recordset.md) method to reopen the object with the same, or modified, attributes.</span></span>

<span data-ttu-id="8919e-123">Enquanto um objeto **Recordset** está fechado, chamar quaisquer métodos que requeiram um cursor dinâmico gera um erro.</span><span class="sxs-lookup"><span data-stu-id="8919e-123">While a **Recordset** object is closed, calling any methods that require a live cursor generates an error.</span></span>

<span data-ttu-id="8919e-p106">Se uma edição estiver em andamento durante o modo de atualização imediata, chamar o método **Close** gera um erro; em vez disso, chame primeiramente o método [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md). Se você fechar o objeto **Recordset** durante o modo de atualização em batch, todas as alterações desde a última chamada a [UpdateBatch](updatebatch-method-ado.md) serão perdidas.</span><span class="sxs-lookup"><span data-stu-id="8919e-p106">If an edit is in progress while in immediate update mode, calling the **Close** method generates an error; instead, call the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method first. If you close the **Recordset** object while in batch update mode, all changes since the last [UpdateBatch](updatebatch-method-ado.md) call are lost.</span></span>

<span data-ttu-id="8919e-126">Se você utilizar o método [Clone](clone-method-ado.md) para criar cópias de um objeto **Recordset** aberto, fechar o original ou um clone não afetará nenhuma das demais cópias.</span><span class="sxs-lookup"><span data-stu-id="8919e-126">If you use the [Clone](clone-method-ado.md) method to create copies of an open **Recordset** object, closing the original or a clone does not affect any of the other copies.</span></span>


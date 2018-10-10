---
title: Mover o método - ActiveX Data Objects (ADO)
TOCTitle: Move Method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 88787d1f76f84db13feea4bac0e8febd2db1e473
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462849"
---
# <a name="move-method-ado"></a><span data-ttu-id="3b54d-102">Método Move (ADO)</span><span class="sxs-lookup"><span data-stu-id="3b54d-102">Move Method (ADO)</span></span>


<span data-ttu-id="3b54d-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b54d-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="3b54d-104">Move a posição do registro atual em um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3b54d-104">Moves the position of the current record in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b54d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b54d-105">Syntax</span></span>

<span data-ttu-id="3b54d-106">*conjunto de registros*. Mover *NumRecords*, *Iniciar*</span><span class="sxs-lookup"><span data-stu-id="3b54d-106">*recordset*.Move *NumRecords*, *Start*</span></span>

## <a name="parameters"></a><span data-ttu-id="3b54d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b54d-107">Parameters</span></span>

  - <span data-ttu-id="3b54d-108">*NumRecords*</span><span class="sxs-lookup"><span data-stu-id="3b54d-108">*NumRecords*</span></span>

  - <span data-ttu-id="3b54d-109">Uma expressão **Long** com sinal que especifica o número de registros que a posição do registro atual é movida.</span><span class="sxs-lookup"><span data-stu-id="3b54d-109">A signed **Long** expression that specifies the number of records that the current record position moves.</span></span>

  - <span data-ttu-id="3b54d-110">*Start*</span><span class="sxs-lookup"><span data-stu-id="3b54d-110">*Start*</span></span>

  - <span data-ttu-id="3b54d-p101">Opcional. Um valor **String** ou **Variant** que é avaliado para um indicador. Também é possível utilizar um valor [BookmarkEnum](bookmarkenum.md).</span><span class="sxs-lookup"><span data-stu-id="3b54d-p101">Optional. A **String** value or **Variant** that evaluates to a bookmark. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b54d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b54d-114">Remarks</span></span>

<span data-ttu-id="3b54d-115">O método **Move** é suportado em todos os objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3b54d-115">The **Move** method is supported on all **Recordset** objects.</span></span>

<span data-ttu-id="3b54d-p102">Se o argumento *NumRecords* for maior que zero, a posição de registro atual é movida para frente (em direção ao final do **Recordset**). Se *NumRecords* for menor que zero, a posição de registro atual será movida para trás (em direção ao início do **Recordset**).</span><span class="sxs-lookup"><span data-stu-id="3b54d-p102">If the *NumRecords* argument is greater than zero, the current record position moves forward (toward the end of the **Recordset**). If *NumRecords* is less than zero, the current record position moves backward (toward the beginning of the **Recordset**).</span></span>

<span data-ttu-id="3b54d-118">Se a chamada **Mover** seria mover a posição do registro atual em um ponto antes do primeiro registro, o ADO define o registro atual para a posição antes do primeiro registro no recordset ([BOF](bof-eof-properties-ado.md) é **verdadeira**).</span><span class="sxs-lookup"><span data-stu-id="3b54d-118">If the **Move** call would move the current record position to a point before the first record, ADO sets the current record to the position before the first record in the recordset ([BOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="3b54d-119">Uma tentativa em mover para trás quando a propriedade **BOF** já é **True** gera um erro.</span><span class="sxs-lookup"><span data-stu-id="3b54d-119">An attempt to move backward when the **BOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="3b54d-120">Se a chamada **Mover** seria mover a posição do registro atual para um ponto após o último registro, o ADO define o registro atual para a posição após o último registro no recordset ([EOF](bof-eof-properties-ado.md) é **True**).</span><span class="sxs-lookup"><span data-stu-id="3b54d-120">If the **Move** call would move the current record position to a point after the last record, ADO sets the current record to the position after the last record in the recordset ([EOF](bof-eof-properties-ado.md) is **True**).</span></span> <span data-ttu-id="3b54d-121">Uma tentativa em mover para frente quando a propriedade **EOF** já é **True** gera um erro.</span><span class="sxs-lookup"><span data-stu-id="3b54d-121">An attempt to move forward when the **EOF** property is already **True** generates an error.</span></span>

<span data-ttu-id="3b54d-122">Chamar o método **Move** a partir de um objeto **Recordset** vazio gera um erro.</span><span class="sxs-lookup"><span data-stu-id="3b54d-122">Calling the **Move** method from an empty **Recordset** object generates an error.</span></span>

<span data-ttu-id="3b54d-123">Se você passar o argumento *Start* , a movimentação é relativo record com este indicador, supondo que o objeto **Recordset** suporta indicadores.</span><span class="sxs-lookup"><span data-stu-id="3b54d-123">If you pass the *Start* argument, the move is relative to the record with this bookmark, assuming the **Recordset** object supports bookmarks.</span></span> <span data-ttu-id="3b54d-124">Se não for especificado, o movimento será relativo ao registro atual.</span><span class="sxs-lookup"><span data-stu-id="3b54d-124">If not specified, the move is relative to the current record.</span></span>

<span data-ttu-id="3b54d-125">Força o ADO para recuperar um novo grupo de registros, se você estiver usando a propriedade [CacheSize](cachesize-property-ado.md) para registros no cache localmente do provedor, passando um argumento *NumRecords* que move a posição do registro atual fora do grupo atual de registros armazenados em cache Iniciando o registro de destino.</span><span class="sxs-lookup"><span data-stu-id="3b54d-125">If you are using the [CacheSize](cachesize-property-ado.md) property to locally cache records from the provider, passing a *NumRecords* argument that moves the current record position outside the current group of cached records forces ADO to retrieve a new group of records, starting from the destination record.</span></span> <span data-ttu-id="3b54d-126">A propriedade **CacheSize** determina o tamanho do grupo recém-recuperado e o registro de destino é o primeiro registro recuperado.</span><span class="sxs-lookup"><span data-stu-id="3b54d-126">The **CacheSize** property determines the size of the newly retrieved group, and the destination record is the first record retrieved.</span></span>

<span data-ttu-id="3b54d-127">Se o objeto **Recordset** for encaminhar apenas, um usuário ainda poderá passar um argumento *NumRecords* menor do que zero, desde que o destino é dentro do conjunto atual de registros armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="3b54d-127">If the **Recordset** object is forward only, a user can still pass a *NumRecords* argument less than zero, provided the destination is within the current set of cached records.</span></span> <span data-ttu-id="3b54d-128">Se a chamada a **Move** moveria a posição do registro atual para um registro antes do primeiro registro em cache, um erro ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="3b54d-128">If the **Move** call would move the current record position to a record before the first cached record, an error will occur.</span></span> <span data-ttu-id="3b54d-129">Dessa forma, é possível utilizar um cache de registro que suporte rolagem total em um provedor que suporte apenas rolagem para frente.</span><span class="sxs-lookup"><span data-stu-id="3b54d-129">Thus, you can use a record cache that supports full scrolling over a provider that supports only forward scrolling.</span></span> <span data-ttu-id="3b54d-130">Como os registros em cache são carregados em memória, você deve evitar o armazenamento em cache de mais registros que o necessário.</span><span class="sxs-lookup"><span data-stu-id="3b54d-130">Because cached records are loaded into memory, you should avoid caching more records than is necessary.</span></span> <span data-ttu-id="3b54d-131">Mesmo se um objeto **Recordset** apenas de avanço suportar movimentos para trás dessa forma, chamar o método [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) em qualquer objeto **Recordset** apenas de avanço ainda gerará um erro.</span><span class="sxs-lookup"><span data-stu-id="3b54d-131">Even if a forward-only **Recordset** object supports backward moves in this way, calling the [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method on any forward-only **Recordset** object will still generate an error.</span></span>


> [!NOTE]
> <span data-ttu-id="3b54d-p108">[!OBSERVAçãO] O suporte para movimentos para trás em um **Recordset** apenas de avanço não é previsível, dependendo do provedor. Se o registro atual foi posicionado após o último registro no **Recordset**, **Move** para trás pode não resultar na posição atual correta.</span><span class="sxs-lookup"><span data-stu-id="3b54d-p108">Support for moving backwards in a forward-only **Recordset** is not predictable, depending upon your provider. If the current record has been postioned after the last record in the **Recordset**, **Move** backwards may not result in the correct current position.</span></span>



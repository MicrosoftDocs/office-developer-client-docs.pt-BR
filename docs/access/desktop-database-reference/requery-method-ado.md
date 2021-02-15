---
title: Método Requery (ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dc236d730cf773ec38fe5dd903cb64ca9b594
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306710"
---
# <a name="requery-method-ado"></a><span data-ttu-id="89564-102">Método Requery (ADO)</span><span class="sxs-lookup"><span data-stu-id="89564-102">Requery method (ADO)</span></span>

<span data-ttu-id="89564-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89564-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89564-104">Atualiza os dados em um objeto [Recordset](recordset-object-ado.md), reexecutando a consulta que serve de base ao objeto.</span><span class="sxs-lookup"><span data-stu-id="89564-104">Updates the data in a [Recordset](recordset-object-ado.md) object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="89564-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89564-105">Syntax</span></span>

<span data-ttu-id="89564-106">*recordset*. Opções de *repetir a configuração*</span><span class="sxs-lookup"><span data-stu-id="89564-106">*recordset*.Requery *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="89564-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89564-107">Parameters</span></span>

|<span data-ttu-id="89564-108">Nome</span><span class="sxs-lookup"><span data-stu-id="89564-108">Name</span></span> |<span data-ttu-id="89564-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="89564-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="89564-110">*Opções*</span><span class="sxs-lookup"><span data-stu-id="89564-110">*Options*</span></span> |<span data-ttu-id="89564-p101">Opcional. Um bitmask contendo os valores [ExecuteOptionEnum](executeoptionenum.md) e [CommandTypeEnum](commandtypeenum.md) que afetam esta operação.</span><span class="sxs-lookup"><span data-stu-id="89564-p101">Optional. A bitmask that contains [ExecuteOptionEnum](executeoptionenum.md) and [CommandTypeEnum](commandtypeenum.md) values affecting this operation.</span></span>|

> [!NOTE]
> <span data-ttu-id="89564-113">Se *Options* for definido como **adAsyncExecute**, essa operação será executada de forma assíncrona e um evento [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) será emitido quando for concluído.</span><span class="sxs-lookup"><span data-stu-id="89564-113">If *Options* is set to **adAsyncExecute**, this operation will execute asynchronously and a [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) event will be issued when it concludes.</span></span>

<span data-ttu-id="89564-114">O valor **adExecuteNoRecords** ou **adExecuteStream** de **ExecuteOpenEnum** não deve ser usado com **Requery**.</span><span class="sxs-lookup"><span data-stu-id="89564-114">The **ExecuteOpenEnum** values of **adExecuteNoRecords** or **adExecuteStream** should not be used with **Requery**.</span></span>

## <a name="remarks"></a><span data-ttu-id="89564-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="89564-115">Remarks</span></span>

<span data-ttu-id="89564-p102">Use o método **Requery** para atualizar todo o conteúdo de um objeto **Recordset** a partir da fonte de dados, emitindo novamente o comando original e recuperando os dados uma segunda vez. A chamada desse método equivale à chamada dos métodos [Close](close-method-ado.md) e [Open](open-method-ado-recordset.md) sucessivamente. Se você estiver editando o registro atual ou adicionando um novo registro, ocorrerá erro.</span><span class="sxs-lookup"><span data-stu-id="89564-p102">Use the **Requery** method to refresh the entire contents of a **Recordset** object from the data source by reissuing the original command and retrieving the data a second time. Calling this method is equivalent to calling the [Close](close-method-ado.md) and [Open](open-method-ado-recordset.md) methods in succession. If you are editing the current record or adding a new record, an error occurs.</span></span>

<span data-ttu-id="89564-p103">Enquanto o objeto **Recordset** estiver aberto, as propriedades que definem a natureza do cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md) etc.) serão somente leitura. Portanto, o método **Requery** somente poderá atualizar o cursor atual. Para alterar qualquer propriedade do cursor e exibir os resultados, use o método [Close](close-method-ado.md) para tornar as propriedades novamente como leitura/gravação. Em seguida, você poderá alterar as configurações de propriedade e chamar o método [Open](open-method-ado-recordset.md) para reabrir o cursor.</span><span class="sxs-lookup"><span data-stu-id="89564-p103">While the **Recordset** object is open, the properties that define the nature of the cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), and so forth) are read-only. Thus, the **Requery** method can only refresh the current cursor. To change any of the cursor properties and view the results, you must use the [Close](close-method-ado.md) method so that the properties become read/write again. You can then change the property settings and call the [Open](open-method-ado-recordset.md) method to reopen the cursor.</span></span>


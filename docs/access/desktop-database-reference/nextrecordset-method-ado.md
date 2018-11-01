---
title: Método NextRecordset (ADO)
TOCTitle: NextRecordset Method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec6b6677e0de89b22f3c35009edcbc05684d10ce
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872596"
---
# <a name="nextrecordset-method-ado"></a><span data-ttu-id="186ab-102">Método NextRecordset (ADO)</span><span class="sxs-lookup"><span data-stu-id="186ab-102">NextRecordset Method (ADO)</span></span>


<span data-ttu-id="186ab-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="186ab-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="186ab-104">Limpa o objeto [Recordset](recordset-object-ado.md) atual e retorna o próximo **Recordset** avançando por uma série de comandos.</span><span class="sxs-lookup"><span data-stu-id="186ab-104">Clears the current [Recordset](recordset-object-ado.md) object and returns the next **Recordset** by advancing through a series of commands.</span></span>

## <a name="syntax"></a><span data-ttu-id="186ab-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="186ab-105">Syntax</span></span>

<span data-ttu-id="186ab-106">Definir *recordset2* = *recordset1*. NextRecordset (*RecordsAffected* )</span><span class="sxs-lookup"><span data-stu-id="186ab-106">Set *recordset2* = *recordset1*.NextRecordset(*RecordsAffected* )</span></span>

## <a name="return-value"></a><span data-ttu-id="186ab-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="186ab-107">Return value</span></span>

<span data-ttu-id="186ab-p101">Retorna um objeto **Recordset**. No modelo de sintaxe, *recordset1* e *recordset2* podem ser o mesmo objeto **Recordset** ou você pode utilizar objetos separados. Ao utilizar objetos **Recordset** separados, redefinir a propriedade **ActiveConnection** no **Recordset** original (*recordset1*) depois que **NextRecordset** for chamado gerará um erro.</span><span class="sxs-lookup"><span data-stu-id="186ab-p101">Returns a **Recordset** object. In the syntax model, *recordset1* and *recordset2* can be the same **Recordset** object, or you can use separate objects. When using separate **Recordset** objects, resetting the **ActiveConnection** property on the original **Recordset** (*recordset1*) after **NextRecordset** has been called will generate an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="186ab-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="186ab-111">Parameters</span></span>

- <span data-ttu-id="186ab-112">*RecordsAffected*</span><span class="sxs-lookup"><span data-stu-id="186ab-112">*RecordsAffected*</span></span>

- <span data-ttu-id="186ab-p102">Opcional. Uma variável **Long** para a qual o provedor retorna o número de registros que a operação atual afetou.</span><span class="sxs-lookup"><span data-stu-id="186ab-p102">Optional. A **Long** variable to which the provider returns the number of records that the current operation affected.</span></span>


> [!NOTE]
> <P><span data-ttu-id="186ab-115">[!OBSERVAçãO] Este parâmetro retorna apenas o número de registros afetados por uma operação; ele não retorna uma contagem dos registros de uma instrução select utilizada para gerar o <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="186ab-115">This parameter only returns the number of records affected by an operation; it does not return a count of records from a select statement used to generate the <STRONG>Recordset</STRONG>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="186ab-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="186ab-116">Remarks</span></span>

<span data-ttu-id="186ab-117">Utilize o método **NextRecordset** para retornar os resultados do próximo comando em uma instrução de comando composta ou de um procedimento armazenado que retorna vários resultados.</span><span class="sxs-lookup"><span data-stu-id="186ab-117">Use the **NextRecordset** method to return the results of the next command in a compound command statement or of a stored procedure that returns multiple results.</span></span> <span data-ttu-id="186ab-118">Se você abrir um objeto **Recordset** baseado em uma instrução de comando compostos (por exemplo, "Selecione \* da tabela 1; Selecione \* de tabela2 ") usando o método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) em um [comando](command-object-ado.md) ou o método [Open](open-method-ado-recordset.md) em um **Recordset**, o ADO apenas o primeiro comando é executado e retorna os resultados para o *conjunto de registros*.</span><span class="sxs-lookup"><span data-stu-id="186ab-118">If you open a **Recordset** object based on a compound command statement (for example, "SELECT \* FROM table1;SELECT \* FROM table2") using the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method on a [Command](command-object-ado.md) or the [Open](open-method-ado-recordset.md) method on a **Recordset**, ADO executes only the first command and returns the results to *recordset*.</span></span> <span data-ttu-id="186ab-119">Para acessar os resultados dos comandos subsequentes na instrução, chame o método **NextRecordset**.</span><span class="sxs-lookup"><span data-stu-id="186ab-119">To access the results of subsequent commands in the statement, call the **NextRecordset** method.</span></span>

<span data-ttu-id="186ab-120">Desde que existam resultados adicionais e que o **Recordset** que contém as instruções compostas não esteja desconectado ou conduzido pelos limites do processo, o método **NextRecordset** continuará a retornar objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="186ab-120">As long as there are additional results and the **Recordset** containing the compound statements is not disconnected or marshaled across process boundaries, the **NextRecordset** method will continue to return **Recordset** objects.</span></span> <span data-ttu-id="186ab-121">Se um comando que retorne linhas for executado com êxito mas não retornar registros, o objeto **Recordset** retornado estará aberto mas vazio.</span><span class="sxs-lookup"><span data-stu-id="186ab-121">If a row-returning command executes successfully but returns no records, the returned **Recordset** object will be open but empty.</span></span> <span data-ttu-id="186ab-122">Teste esse caso verificando se as propriedades [BOF](bof-eof-properties-ado.md) e [EOF](bof-eof-properties-ado.md) são ambas **True**.</span><span class="sxs-lookup"><span data-stu-id="186ab-122">Test for this case by verifying that the [BOF](bof-eof-properties-ado.md) and [EOF](bof-eof-properties-ado.md) properties are both **True**.</span></span> <span data-ttu-id="186ab-123">Se um comando que não retorne linhas é executado com êxito, o objeto **Recordset** retornado será fechado, que você pode verificar Testando a propriedade [State](state-property-ado.md) no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="186ab-123">If a non–row-returning command executes successfully, the returned **Recordset** object will be closed, which you can verify by testing the [State](state-property-ado.md) property on the **Recordset**.</span></span> <span data-ttu-id="186ab-124">Quando não houver nenhum resultado mais, *recordset* será definido como *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="186ab-124">When there are no more results, *recordset* will be set to *Nothing*.</span></span>

<span data-ttu-id="186ab-125">O método **NextRecordset** não está disponível em um objeto **Recordset** desconectado, em que [ActiveConnection](activeconnection-property-ado.md) foi definido como **Nothing** (no Microsoft Visual Basic) ou NULL (em outras linguagens).</span><span class="sxs-lookup"><span data-stu-id="186ab-125">The **NextRecordset** method is not available on a disconnected **Recordset** object, where [ActiveConnection](activeconnection-property-ado.md) has been set to **Nothing** (in Microsoft Visual Basic) or NULL (in other languages).</span></span>

<span data-ttu-id="186ab-126">Se uma edição estiver em andamento durante o modo de atualização imediata, chamar o método **NextRecordset** gera um erro; chame primeiramente o método [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="186ab-126">If an edit is in progress while in immediate update mode, calling the **NextRecordset** method generates an error; call the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method first.</span></span>

<span data-ttu-id="186ab-p105">Para passar parâmetros para mais de um comando na instrução composta por meio do preenchimento da coleção [Parameters](parameters-collection-ado.md) ou passando-se uma matriz com a chamada a **Open** ou **Execute** original, os parâmetros devem estar na mesma ordem na coleção ou matriz que seus respectivos comandos na série de comandos. Primeiro é necessário terminar de ler todos os resultados antes de ler os valores do parâmetro de saída.</span><span class="sxs-lookup"><span data-stu-id="186ab-p105">To pass parameters for more than one command in the compound statement by filling the [Parameters](parameters-collection-ado.md) collection, or by passing an array with the original **Open** or **Execute** call, the parameters must be in the same order in the collection or array as their respective commands in the command series. You must finish reading all the results before reading output parameter values.</span></span>

<span data-ttu-id="186ab-p106">O provedor de banco de dados OLE determina quando cada comando em uma instrução composta é executado. O [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), por exemplo, executa todos os comandos em um lote após o recebimento da instrução composta. Os **Recordsets** resultantes serão simplesmente retornados quando você chamar **NextRecordset**.</span><span class="sxs-lookup"><span data-stu-id="186ab-p106">Your OLE DB provider determines when each command command in a compound statement is executed. The [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), for example, executes all commands in a batch upon receiving the compound statement. The resulting **Recordsets** are simply returned when you call **NextRecordset**.</span></span>

<span data-ttu-id="186ab-p107">No entanto, outros provedores poderão executar o próximo comando em uma instrução somente depois que NextRecordset for chamado. Para esses provedores, se você fechar explicitamente o objeto **Recordset** antes de percorrer por etapas a instrução de comando inteira, o ADO nunca executará os comandos restantes.</span><span class="sxs-lookup"><span data-stu-id="186ab-p107">However, other providers may execute the next command in a statement only after NextRecordset is called. For these providers, if you explicitly close the **Recordset** object before stepping through the entire command statement, ADO never executes the remaining commands.</span></span>


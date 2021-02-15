---
title: Método NextRecordset (ADO)
TOCTitle: NextRecordset method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b572f4ebe55da1add781ecd86df97937cfeae126
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288614"
---
# <a name="nextrecordset-method-ado"></a>Método NextRecordset (ADO)

**Aplica-se ao:** Access 2013, Office 2013
 
Limpa o objeto [Recordset](recordset-object-ado.md) atual e retorna o próximo **Recordset** avançando por uma série de comandos.

## <a name="syntax"></a>Sintaxe

Definir *recordset2*  =  *recordset1*. NextRecordset(*RecordsAffected* )

## <a name="return-value"></a>Valor de retorno

Retorna um objeto **Recordset**. No modelo de sintaxe, *recordset1* e *recordset2* podem ser o mesmo objeto **Recordset** ou você pode utilizar objetos separados. Ao utilizar objetos **Recordset** separados, redefinir a propriedade **ActiveConnection** no **Recordset** original (*recordset1*) depois que **NextRecordset** for chamado gerará um erro.

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*RecordsAffected* |Opcional. Uma variável **Long** para a qual o provedor retorna o número de registros que a operação atual afetou.|

> [!NOTE]
> [!OBSERVAçãO] Este parâmetro retorna apenas o número de registros afetados por uma operação; ele não retorna uma contagem dos registros de uma instrução select utilizada para gerar o **Recordset**.

## <a name="remarks"></a>Comentários

Utilize o método **NextRecordset** para retornar os resultados do próximo comando em uma instrução de comando composta ou de um procedimento armazenado que retorna vários resultados. Se você abrir um **objeto Recordset** com base em uma instrução de comando composta (por exemplo, "SELECT \* FROM table1; SELECT \* FROM table2") using the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method on a [Command](command-object-ado.md) or the [Open](open-method-ado-recordset.md) method on a **Recordset**, ADO executes only the first command and returns the results to *recordset*. Para acessar os resultados dos comandos subsequentes na instrução, chame o método **NextRecordset**.

Desde que existam resultados adicionais e que o **Recordset** que contém as instruções compostas não esteja desconectado ou conduzido pelos limites do processo, o método **NextRecordset** continuará a retornar objetos **Recordset**. Se um comando que retorne linhas for executado com êxito mas não retornar registros, o objeto **Recordset** retornado estará aberto mas vazio. Teste esse caso verificando se as propriedades [BOF](bof-eof-properties-ado.md) e [EOF](bof-eof-properties-ado.md) são ambas **True**. Se um comando que não retorne linhas for executado com êxito, o objeto **Recordset** retornado estará fechado, o que pode ser verificado pelo teste da propriedade [State](state-property-ado.md) no **Recordset**. Quando não mais existirem resultados, *recordset* será definido como *Nothing*.

O método **NextRecordset** não está disponível em um objeto **Recordset** desconectado, em que [ActiveConnection](activeconnection-property-ado.md) foi definido como **Nothing** (no Microsoft Visual Basic) ou NULL (em outras linguagens).

Se uma edição estiver em andamento durante o modo de atualização imediata, chamar o método **NextRecordset** gera um erro; chame primeiramente o método [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md).

Para passar parâmetros para mais de um comando na instrução composta por meio do preenchimento da coleção [Parameters](parameters-collection-ado.md) ou passando-se uma matriz com a chamada a **Open** ou **Execute** original, os parâmetros devem estar na mesma ordem na coleção ou matriz que seus respectivos comandos na série de comandos. Primeiro é necessário terminar de ler todos os resultados antes de ler os valores do parâmetro de saída.

O provedor de banco de dados OLE determina quando cada comando em uma instrução composta é executado. O [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), por exemplo, executa todos os comandos em um lote após o recebimento da instrução composta. Os **Recordsets** resultantes serão simplesmente retornados quando você chamar **NextRecordset**.

No entanto, outros provedores poderão executar o próximo comando em uma instrução somente depois que NextRecordset for chamado. Para esses provedores, se você fechar explicitamente o objeto **Recordset** antes de percorrer por etapas a instrução de comando inteira, o ADO nunca executará os comandos restantes.


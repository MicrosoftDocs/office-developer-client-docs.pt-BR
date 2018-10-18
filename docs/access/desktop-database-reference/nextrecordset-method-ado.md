---
title: Método NextRecordset (ADO)
TOCTitle: NextRecordset Method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e412fbcb083e4cf5acae363ef05ce11ad9754215
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603396"
---
# <a name="nextrecordset-method-ado"></a>Método NextRecordset (ADO)


**Aplica-se a**: Access 2013 | Office 2013
 

Limpa o objeto [Recordset](recordset-object-ado.md) atual e retorna o próximo **Recordset** avançando por uma série de comandos.

## <a name="syntax"></a>Sintaxe

Definir *recordset2* = *recordset1*. NextRecordset (*RecordsAffected* )

<<<<<<< Cabeça
## <a name="return-value"></a>Valor retornado
=======
## <a name="return-value"></a>Valor de retorno
>>>>>>> mestre

Retorna um objeto **Recordset**. No modelo de sintaxe, *recordset1* e *recordset2* podem ser o mesmo objeto **Recordset** ou você pode utilizar objetos separados. Ao utilizar objetos **Recordset** separados, redefinir a propriedade **ActiveConnection** no **Recordset** original (*recordset1*) depois que **NextRecordset** for chamado gerará um erro.

## <a name="parameters"></a>Parâmetros

- *RecordsAffected*

- Opcional. Uma variável **Long** para a qual o provedor retorna o número de registros que a operação atual afetou.


> [!NOTE]
> <P>[!OBSERVAçãO] Este parâmetro retorna apenas o número de registros afetados por uma operação; ele não retorna uma contagem dos registros de uma instrução select utilizada para gerar o <STRONG>Recordset</STRONG>.</P>



## <a name="remarks"></a>Comentários

<<<<<<< Cabeça Use o método **NextRecordset** para apresentar os resultados do próximo comando em uma instrução de comando compostos ou de um procedimento armazenado que retorna vários resultados. Se você abrir um objeto **Recordset** baseado em uma instrução de comando compostos (por exemplo, "Selecione \* da tabela 1; Selecione \* de tabela2 ") usando o método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) em um [comando](command-object-ado.md) ou o método [Open](open-method-ado-recordset.md) em um **Recordset**, o ADO apenas o primeiro comando é executado e retorna os resultados para o *conjunto de registros*. Para acessar os resultados dos comandos subsequentes na instrução, chame o método **NextRecordset**.
=== Use o método **NextRecordset** para apresentar os resultados do próximo comando em uma instrução de comando compostos ou de um procedimento armazenado que retorna vários resultados. Se você abrir um objeto **Recordset** baseado em uma instrução de comando compostos (por exemplo, "Selecione \* da tabela 1; Selecione \* de tabela2 ") usando o método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) em um [comando](command-object-ado.md) ou o método [Open](open-method-ado-recordset.md) em um **Recordset**, o ADO apenas o primeiro comando é executado e retorna os resultados para o *conjunto de registros*. Para acessar os resultados dos comandos subsequentes na instrução, chame o método **NextRecordset**.
>>>>>>> mestre

Desde que existam resultados adicionais e que o **Recordset** que contém as instruções compostas não esteja desconectado ou conduzido pelos limites do processo, o método **NextRecordset** continuará a retornar objetos **Recordset**. Se um comando que retorne linhas for executado com êxito mas não retornar registros, o objeto **Recordset** retornado estará aberto mas vazio. Teste esse caso verificando se as propriedades [BOF](bof-eof-properties-ado.md) e [EOF](bof-eof-properties-ado.md) são ambas **True**. Se um comando que não retorne linhas é executado com êxito, o objeto **Recordset** retornado será fechado, que você pode verificar Testando a propriedade [State](state-property-ado.md) no **Recordset**. Quando não houver nenhum resultado mais, *recordset* será definido como *Nothing*.

O método **NextRecordset** não está disponível em um objeto **Recordset** desconectado, em que [ActiveConnection](activeconnection-property-ado.md) foi definido como **Nothing** (no Microsoft Visual Basic) ou NULL (em outras linguagens).

Se uma edição estiver em andamento durante o modo de atualização imediata, chamar o método **NextRecordset** gera um erro; chame primeiramente o método [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md).

Para passar parâmetros para mais de um comando na instrução composta por meio do preenchimento da coleção [Parameters](parameters-collection-ado.md) ou passando-se uma matriz com a chamada a **Open** ou **Execute** original, os parâmetros devem estar na mesma ordem na coleção ou matriz que seus respectivos comandos na série de comandos. Primeiro é necessário terminar de ler todos os resultados antes de ler os valores do parâmetro de saída.

O provedor de banco de dados OLE determina quando cada comando em uma instrução composta é executado. O [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), por exemplo, executa todos os comandos em um lote após o recebimento da instrução composta. Os **Recordsets** resultantes serão simplesmente retornados quando você chamar **NextRecordset**.

No entanto, outros provedores poderão executar o próximo comando em uma instrução somente depois que NextRecordset for chamado. Para esses provedores, se você fechar explicitamente o objeto **Recordset** antes de percorrer por etapas a instrução de comando inteira, o ADO nunca executará os comandos restantes.


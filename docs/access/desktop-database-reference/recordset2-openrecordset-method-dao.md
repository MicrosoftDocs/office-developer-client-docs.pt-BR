---
title: Método Recordset2.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: da6ce86e-957e-21f8-07ac-8acd57326a12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835325(v=office.15)
ms:contentKeyID: 48548082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08120f4ebb6b2d9989051171a0c71b6d9fcf6e5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307249"
---
# <a name="recordset2openrecordset-method-dao"></a>Método Recordset2.OpenRecordset (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Cria um novo objeto **[Conjunto de registros](recordset-object-dao.md)** e o acrescentar à coleção **Conjuntos de registros**.

## <a name="syntax"></a>Sintaxe

*expressão* .OpenRecordset(***Tipo***, ***Opções***)

*expressão* Uma variável que representa **um objeto Recordset2** .

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Necessária/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>A origem dos registros para o novo <strong>Recordset</strong>. A origem pode ser um nome de tabela, um nome de consulta ou uma instrução SQL que retorna registros. Para objetos de <strong>Recordset</strong> do tipo tabela nos mecanismos de banco de dados do Microsoft Access, a origem pode ser apenas um nome de tabela.</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica que tipo de <strong>Recordset</strong> abrir.</p><p><strong>OBSERVAÇÃO</strong>: Se você abrir um <STRONG>Conjunto de Registros</STRONG> em um espaço de trabalho do Microsoft Access e não especificar um tipo, o <STRONG>OpenRecordset</STRONG> criará uma tabela do tipo <STRONG>Conjunto de Registros</STRONG>, se possível. If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>Opções</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma combinação de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica as características do novo <strong>Recordset</strong>.</p><p><strong>OBSERVAÇÃO</strong>: As constantes <STRONG>dbConsistent</STRONG> e <STRONG>dbInconsistent</STRONG> são mutuamente exclusivas e usar ambas causará um erro. Fornecer um argumento lockedits quando opções usa a constante <STRONG>dbReadOnly</STRONG> também causará um erro.</p>
</td>
</tr>
<tr class="even">
<td><p><em>LockEdit</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina o bloqueio do <strong>Recordset</strong>.</p><p><strong>OBSERVAÇÃO</strong>: você pode usar a constante <STRONG>dbReadOnly</STRONG> tanto no argumento opções quanto no lockedits, mas não em ambos. Se você usá-la para ambos argumentos, ocorrerá um erro de tempo de execução.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor de retorno

Conjunto de Registros

## <a name="remarks"></a>Comentários

Normalmente, se o usuário receber este erro durante a atualização de um registro, seu código deverá atualizar o conteúdo dos campos e recuperar os valores modificados recentemente. Se o erro ocorrer durante a exclusão de um registro, o código poderá exibir os novos dados de registro para o usuário e uma mensagem indicando que os dados foram alterados recentemente. Nesse momento, seu código pode solicitar uma confirmação de que o usuário ainda deseja excluir o registro.

Você também deve usar a constante **dbSeeChanges** se for abrir um **Recordset** em um espaço de trabalho ODBC conectado ao mecanismo do banco de dados do Microsoft Access versus uma tabela do Microsoft SQL Server 6.0 (ou posterior) com uma coluna IDENTIDADE, caso contrário pode resultar em um erro.

Abrir mais de um  **Recordset** em uma origem de dados ODBC pode falhar porque a conexão está ocupada com uma chamada **OpenRecordset** anterior. Uma maneira de evitar isso é preenchendo completamente o **Recordset** usando o método **MoveLast** assim que o **Recordset** for aberto.

Fechar o **Recordset** com o método **[Close](connection-close-method-dao.md)** o exclui automaticamente da coleção de **Recordsets**.

> [!NOTE]
> Se a *fonte* se referir a uma instrução SQL composta por uma sequência concatenada e com um valor não inteiro, e se os parâmetros do sistema especificarem um caractere decimal não-EUA, como uma vírgula (por exemplo, strSQL = "PRICE &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar abrir o **Conjunto de Registros**. Isso se deve ao fato de que, durante a concatenação, o número é convertido em uma cadeia de caracteres usando o caractere decimal padrão do seu sistema, e o SQL aceita apenas caracteres decimais americanos.



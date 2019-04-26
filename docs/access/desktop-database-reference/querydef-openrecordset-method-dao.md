---
title: Método QueryDef.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a046359f39611e38b9e517495f54041f876addfc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302846"
---
# <a name="querydefopenrecordset-method-dao"></a>Método QueryDef.OpenRecordset (DAO)

**Aplica-se ao**: Access 2013, Office 2013

Cria um novo objeto **[Conjunto de registros](recordset-object-dao.md)** e o acrescentar à coleção **Conjuntos de registros**.

## <a name="syntax"></a>Sintaxe

*expressão* .OpenRecordset(***Tipo***, ***Opções***, ***LockEdit***)

*expressão* uma variável que representa um objeto **QueryDef**.

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
<th><p>Necessário/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Type</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica que tipo de <strong>Recordset</strong> abrir.</p><p><strong>OBSERVAÇÃO</strong>: Se você abrir um <STRONG>Conjunto de Registros</STRONG> em um espaço de trabalho do Microsoft Access e não especificar um tipo, o <STRONG>OpenRecordset</STRONG> criará uma tabela do tipo <STRONG>Conjunto de Registros</STRONG>, se possível. If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</p>
</td>
</tr>
<tr class="even">
<td><p><em>Opções</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma combinação de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica as características do novo <strong>Recordset</strong>.</p></p><p><strong>OBSERVAÇÃO</strong>: As constantes <STRONG>dbConsistent</STRONG> e <STRONG>dbInconsistent</STRONG> são mutuamente exclusivas e usar ambas causará um erro. Fornecer um argumento lockedits quando opções usa a constante <STRONG>dbReadOnly</STRONG> também causará um erro.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>LockEdit</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina o bloqueio do <strong>Recordset</strong>.</p></p><p><strong>OBSERVAÇÃO</strong>: você pode usar a constante <STRONG>dbReadOnly</STRONG> tanto no argumento opções quanto no lockedits, mas não em ambos. Se você usá-la para ambos argumentos, ocorrerá um erro de tempo de execução.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor de retorno

Conjunto de Registros

## <a name="remarks"></a>Comentários

Você também deverá usar a constante **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** se abrir um **Recordset** em um espaço de trabalho ODBC conectado ao mecanismo de banco de dados do Microsoft Access em uma tabela do Microsoft SQL Server 6.0 (ou posterior), que tenha uma coluna IDENTITY; caso contrário, ocorrerá um erro.

Abrir mais de um **Recordset** em uma fonte de dados ODBC pode falhar porque a conexão está ocupada com uma chamada **OpenRecordset** anterior. Uma forma de contornar essa situação é preencher totalmente o **Recordset** usando o método **[MoveLast](recordset-movelast-method-dao.md)** assim que o **Recordset** for aberto.

Fechar um **Recordset** com o método **Close** o exclui automaticamente da coleção **Recordsets**.

> [!NOTE]
> Se a *fonte* se referir a uma instrução SQL composta por uma sequência concatenada com um valor não inteiro e se os parâmetros do sistema especificarem um caractere decimal não-EUA, como uma vírgula (por exemplo, strSQL = "PRICE &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar abrir o **Conjunto de Registros**. Isso se deve ao fato de que, durante a concatenação, o número é convertido em uma cadeia de caracteres usando o caractere decimal padrão do seu sistema, e o SQL aceita apenas caracteres decimais americanos.



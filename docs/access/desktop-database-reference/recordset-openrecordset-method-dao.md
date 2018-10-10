---
title: Método Recordset.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 7d5ca4d5-5a0b-c0c8-d8e8-2c4e6c5f361f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196402(v=office.15)
ms:contentKeyID: 48545853
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d739eeacc1ceaa90bdc4b5fb58f8d2919484b706
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465431"
---
# <a name="recordsetopenrecordset-method-dao"></a>Método Recordset.OpenRecordset (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Cria e anexa um novo objeto **[Recordset](recordset-object-dao.md)** à coleção **Recordsets**.

## <a name="syntax"></a>Sintaxe

*expressão* . OpenRecordset (***tipo***, ***Opções***)

*expressão* Uma variável que representa um objeto **Recordset** .

### <a name="parameters"></a>Parâmetros

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
<th><p>Obrigatório/Opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>A origem dos registros para o novo <strong>Recordset</strong>. A origem pode ser um nome de tabela, um nome de consulta ou uma instrução SQL que retorna registros. Para objetos de <strong>Recordset</strong> do tipo tabela nos mecanismos de banco de dados do Microsoft Access, a origem pode ser apenas um nome de tabela.  </p></td>
</tr>
<tr class="even">
<td><p>Tipo</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> que indica que tipo de <strong>Recordset</strong> abrir.</p>

> [!NOTE]
> <P>Se você abrir um <STRONG>Recordset</STRONG> em um espaço de trabalho do Microsoft Access se especificar um tipo, o método <STRONG>OpenRecordset</STRONG> criará um <STRONG>Recordset</STRONG> do tipo tabela, se possível. Se você especificar uma consulta ou tabela vinculada, o método <STRONG>OpenRecordset</STRONG> criará um <STRONG>Recordset</STRONG> do tipo dynaset.</P>


</td>
</tr>
<tr class="odd">
<td><p>Options</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma combinação de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> que especifica as características do novo <strong>Recordset</strong>.</p>

> [!NOTE]
> <P>As constantes <STRONG>dbConsistent</STRONG> e <STRONG>dbInconsistent</STRONG> são mutuamente exclusivos e usando os dois causará um erro. Também fornecer um argumento lockedits quando opções usa a constante <STRONG>dbReadOnly</STRONG> causará um erro.</P>


</td>
</tr>
<tr class="even">
<td><p>LockEdit</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> que determina o bloqueio do <strong>Recordset</strong>.</p>

> [!NOTE]
> <P>Você pode usar <STRONG>dbReadOnly</STRONG> no argumento options ou o argumento lockedits, mas não ambos. Se você usá-lo para ambos os argumentos, ocorrerá um erro em tempo de execução.</P>


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor de Retorno

Recordset

## <a name="remarks"></a>Comentários

Normalmente, se o usuário obtém esse erro ao atualizar um registro, seu código deve atualizar o conteúdo dos campos e recuperar os valores modificados recentemente. Se o erro ocorrer ao excluir um registro, seu código poderá exibir os dados do novo registro para o usuário e uma mensagem indicando que os dados foram alterados recentemente. Nesse momento, seu código pode solicitar uma confirmação de que o usuário ainda deseja excluir o registro.

Você também deverá usar a constante **dbSeeChanges** se abrir um **Recordset** em um espaço de trabalho ODBC conectado ao mecanismo de banco de dados do Microsoft Access em uma tabela do Microsoft SQL Server 6.0 (ou posterior), que tenha uma coluna IDENTITY; caso contrário, ocorrerá um erro.

Abrir mais de um **Recordset** em uma fonte de dados ODBC pode falhar porque a conexão está ocupada com uma chamada **OpenRecordset** anterior. Uma forma de contornar essa situação é preencher totalmente o **Recordset** usando o método **MoveLast** assim que o **Recordset** for aberto.

Fechar um **Recordset** com o método **[Close](connection-close-method-dao.md)** o exclui automaticamente da coleção **Recordsets**.


> [!NOTE]
> <P>Se a <EM>fonte</EM> refere-se a uma instrução SQL composto por uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal que fora dos EUA, como uma vírgula (por exemplo, strSQL = "preço &gt; " &amp; lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar abrir o <STRONG>Recordset</STRONG>. Isso ocorre porque durante a concatenação, o número é convertido para uma sequência utilizando o caractere decimal padrão do seu sistema, e o SQL aceita apenas caracteres decimais EUA.</P>



---
title: Método Recordset2.FindNext (DAO)
TOCTitle: FindNext Method
ms:assetid: dc1d9fdf-36ae-cb23-4949-f7b98cb5d4e2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835354(v=office.15)
ms:contentKeyID: 48548121
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d1f947850f0df1d50031cbab43b2336fa5ecaec
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883467"
---
# <a name="recordset2findnext-method-dao"></a>Método Recordset2.FindNext (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Localiza o próximo registro em um objeto **[Recordset](recordset-object-dao.md)** tipo dynaset ou instantâneo que atenda a critérios específicos e torne esse registro o registro atual (apenas espaços de trabalho do Microsoft Access ). .

## <a name="syntax"></a>Sintaxe

*expressão* . FindNext (***critérios***)

*expressão* Uma variável que representa um objeto **Recordset2** .

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
<td><p>Criteria</p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>Cadeia de caracteres</strong></p></td>
<td><p>Uma sequência usada para localizar o registro. Ela é como a cláusula WHERE em uma instrução SQL, mas sem a palavra WHERE.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Se desejar incluir todos os registros em sua pesquisa, além dos que atendem às condições específicas, use os métodos **Move** para se mover entre registros. Para localizar um registro em um **Conjunto de registros** de tipo tabela, use o método **Buscar**.

Se a correspondência de critérios do registro não for localizada, o indicador do registro atual será desconhecido e a propriedade **Nenhuma correspondência** será definida como **Verdadeiro**. Se o conjunto de registros incluir mais de um registro que satisfaça os critérios, o **FindFirst** vai localizar a primeira ocorrência, o **FindNext** vai localizar a próxima ocorrência, e assim por diante.

Todos os métodos **Find** iniciam suas pesquisas a partir do local e na direção especificada na tabela a seguir.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Método Find</p></th>
<th><p>Inicia pesquisa em</p></th>
<th><p>Direção da pesquisa</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>FindFirst</strong></p></td>
<td><p>Início do conjunto de registros</p></td>
<td><p>Fim do conjunto de registros</p></td>
</tr>
<tr class="even">
<td><p><strong>FindLast</strong></p></td>
<td><p>Fim do conjunto de registros</p></td>
<td><p>Início do conjunto de registros</p></td>
</tr>
<tr class="odd">
<td><p><strong>FindNext</strong></p></td>
<td><p>Registro atual</p></td>
<td><p>Fim do conjunto de registros</p></td>
</tr>
<tr class="even">
<td><p><strong>FindPrevious</strong></p></td>
<td><p>Registro atual</p></td>
<td><p>Início do conjunto de registros</p></td>
</tr>
</tbody>
</table>


No entanto, utilizar um dos métodos **Find** não é o mesmo que utilizar um método **Move**, que simplesmente torna atual o primeiro, o último, o anterior ou o próximo registro sem especificar uma condição. A operação Find pode ser seguida pela operação Move.

Sempre verifique o valor da propriedade **NoMatch** para determinar se a operação Find foi bem-sucedida. Se a pesquisa for bem-sucedida, **NoMatch** será **False**. Se ela falhar, **NoMatch** será **True**, e o registro atual não será definido. Nesse caso, você deve posicionar o ponteiro atual do registro de volta em um registro válido.

Utilizar o método **Find** com os conjuntos de registros com acesso ODBC conectados por mecanismo do banco de dados do Microsoft Access pode não ser eficaz. Você poderá constatar que reformular os critérios para localizar um registro específico seja mais rápido, especialmente quando se trabalha com grandes conjuntos de registros.

Ao trabalhar com os bancos de dados com acesso ODBC conectados por mecanismo do banco de dados do Microsoft Access e por grande objetos tipo dynaset do **Conjunto de registros**, você poderá descobrir que usar os métodos **Find** ou as propriedades **Classificar** ou **Filtrar** é mais lento. Para melhorar o desempenho, use as consultas SQL cláusulas ORDER BY ou WHERE, consultas de parâmetro ou objetos **QueryDef** personalizados, que recuperam registros específicos indexados.

Você deve usar o formato de data americano (mês-dia-ano) ao pesquisar campos contendo datas, mesmo que não esteja utilizando uma versão em inglês do mecanismo de banco de dados do Microsoft Access; caso contrário, os dados não poderão ser localizado. Use a função **Format** do Visual Basic para converter a data. Por exemplo:

```vb
rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

Se os critérios é composta por uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal que fora dos EUA, como uma vírgula (por exemplo, strSQL = "preço \> " & lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar Chame o método. Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.


> [!NOTE]
> <UL>
> <LI>
> <P>Para melhor desempenho, os <EM>critérios</EM> devem estar em um formato "<EM>campo</EM> = <EM>valor</EM>" onde o <EM>campo</EM> é um campo indexado na tabela base ou "<EM>campo</EM> como <EM>prefixo</EM>" onde o <EM>campo</EM> é um campo indexado na tabela base e <EM>prefixo</EM> é uma cadeia de caracteres de pesquisa do prefixo (por exemplo, "ART *").</P>
> <LI>
> <P>Em geral, para tipos equivalentes de pesquisa, o método <STRONG>Seek</STRONG> fornece melhor desempenho que os métodos <STRONG>Find</STRONG>. Isso significa que os objetos <STRONG>Recordset</STRONG> tipo tabela sozinhos podem atender às suas necessidades.</P></LI></UL>



---
title: Método Recordset.FindNext (DAO)
TOCTitle: FindNext Method
ms:assetid: 5457dfc8-e561-5624-74d0-34278ba2e7cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194099(v=office.15)
ms:contentKeyID: 48544893
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d9e4651b2fb5fa9f0ef8569b9f4b28d4c031e87
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885294"
---
# <a name="recordsetfindnext-method-dao"></a>Método Recordset.FindNext (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Localiza o próximo registro em um objeto **[Recordset](recordset-object-dao.md)** tipo dynaset ou instantâneo que atenda a critérios específicos e torne esse registro o registro atual (apenas espaços de trabalho do Microsoft Access ).

## <a name="syntax"></a>Sintaxe

*expressão* . FindNext (***critérios***)

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

Em um espaço de trabalho ODBCDirect, os métodos **Find** e **Seek** não estão disponíveis em nenhum tipo de objeto **Recordset**, porque executar um método **Find** ou **Seek** por meio de uma conexão ODBC não é muito eficiente na rede. Em vez disso, você deve projetar a consulta (ou seja, usando o argumento de origem para o método **OpenRecordset** ) com uma cláusula WHERE adequada que restringe os registros retornados somente aquelas que atendam aos critérios caso contrário, seria usado em um **Localizar** ou Método **Seek** .

Ao trabalhar com bancos de dados ODBC conectados ao mecanismo de banco de dados do Microsoft Access e com grandes objetos v tipo dynaset, você poderá descobrir que a utilização dos métodos **Find** ou da propriedade **Sort** ou **Filter** é lenta. Para aprimorar o desempenho, use as consultas SQL com cláusulas ORDER BY ou WHERE personalizadas, consultas de parâmetro ou objetos **QueryDef** que recuperam registros específicos e indexados.

Você deve usar o formato de data americano (mês-dia-ano) ao pesquisar campos contendo datas, mesmo que não esteja utilizando uma versão em inglês do mecanismo de banco de dados do Microsoft Access; caso contrário, os dados não poderão ser localizado. Use a função **Format** do Visual Basic para converter a data. Por exemplo:

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

Se os critérios é composta por uma cadeia de caracteres concatenada com um valor não inteiro e os parâmetros do sistema especificarem um caractere decimal que fora dos EUA, como uma vírgula (por exemplo, strSQL = "preço \> " & lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar Chame o método. Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.

> [!NOTE]
> - Para melhor desempenho, os *critérios* devem estar em um formato "*campo* = *valor*" onde o *campo* é um campo indexado na tabela base ou "*campo* como *prefixo*" onde o *campo* é um campo indexado na tabela base e *prefixo* é uma cadeia de caracteres de pesquisa do prefixo (por exemplo, "ART *").
> 
> - Em geral, para tipos equivalentes de pesquisa, o método **Seek** fornece melhor desempenho que os métodos **Find**. Isso significa que os objetos **Recordset** tipo tabela sozinhos podem atender às suas necessidades.


## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar os métodos FindFirst e FindNext para localizar um registro em um Recordset.

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).


```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```

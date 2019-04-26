---
title: Método Recordset.FindFirst (DAO)
TOCTitle: FindFirst Method
ms:assetid: 5fcf78cd-7d2c-2e47-14e5-996f2e14ff51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194787(v=office.15)
ms:contentKeyID: 48545170
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b2e334dcad84d2a9c3441e76e6552c1cb04f8552
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300529"
---
# <a name="recordsetfindfirst-method-dao"></a>Método Recordset.FindFirst (DAO)

**Aplica-se ao**: Access 2013, Office 2013

Localiza o primeiro registro em um dynaset ou objeto de tipo instantâneo do **Conjunto de registros**, que atende aos critérios específicos e torna esse registro atual (somente para espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* .FindFirst(***Criteria***)

*expressão* Uma variável que representa um objeto **Recordset**.

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
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Criteria</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
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

É necessário usar o formato de data dos EUA (mês/dia/ano), ao pesquisar campos contendo datas, mesmo se não estiver usando a versão norte-americana do mecanismo de banco de dados do Microsoft Access; caso contrário, os dados podem não ser encontrados. Use a função **Formato** do Visual Basic para converter a data. Por exemplo:

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

Se o critério for composto por uma cadeia concatenada de caracteres e com um valor não inteiro, e se os parâmetros do sistema especificarem um caractere decimal não-EUA, como uma vírgula (por exemplo, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), ocorrerá um erro ao tentar chamar o método. Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.


> [!NOTE]
> - Para melhorar o desempenho, *criteria* deve estar no formato "*field* = *value*", no qual *field* é um campo indexado na tabela base, ou no formato "*field* LIKE *prefix*", no qual *field* é um campo indexado na tabela base e *prefix* é uma sequência de pesquisa de prefixo (por exemplo, "ART*" ).
> 
> - De modo geral, para os tipos de pesquisas, o método **Seek** proporciona um melhor desempenho do que o método **Find**. Isso supõe que os objetos de tipo de tabela **Conjunto de registros** sozinhos podem atender às suas necessidades.


## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar os métodos FindFirst e FindNext para localizar um registro em um Conjunto de Registros.

**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

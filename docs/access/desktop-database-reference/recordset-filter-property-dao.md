---
title: Propriedade Recordset.Filter (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35ae33c9b7979e6dd98d94652a61c8737397c7a3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884300"
---
# <a name="recordsetfilter-property-dao"></a>Propriedade Recordset.Filter (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Define ou retornar um valor que determina os registros incluídos em um objeto **Recordset** aberto subsequentemente (somente espaços de trabalho do Microsoft Access). **String** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . Filtro

*expressão* Uma expressão que retorna um objeto **Recordset** .

## <a name="remarks"></a>Comentários

O valor de definição ou de retorno é um tipo de dados de cadeia de caracteres que contém a cláusula WHERE de uma instrução SQL sem a palavra reservada WHERE.

Use a propriedade **Filter** para aplicar um filtro a um dynaset, instantâneo ou objeto **Recordset** do tipo somente encaminhamento.

Você pode usar a propriedade **Filter** para restringir os registros retornados de um objeto existente quando um novo objeto **Recordset** for aberto com base em um objeto **Recordset** existente.

Utilize o formato de data dos EUA (mês-dia-ano) quando filtrar campos que contenham datas, mesmo se você não estiver usando a versão EUA do mecanismo de banco de dados do Microsoft Access (nesse caso, você deve montar quaisquer datas concatenando cadeias de caracteres, por exemplo, strMonth & "-" & strDay & "-" & strYear). Caso contrário, é possível que os dados não sejam filtrados como esperado.

Em vários casos, é mais rápido abrir um novo objeto **Recordset** usando uma instrução SQL que inclua uma cláusula WHERE.

Se você definir a propriedade como uma cadeia de caracteres concatenada com um valor não – inteiro e os parâmetros do sistema especificarem um caractere decimal que fora dos EUA, como uma vírgula (por exemplo, strFilter = "preço \> " & lngPrice e lngPrice = 125,50), ocorrerá um erro ao tentar Abra o próximo **Recordset**. Isso acontecerá porque durante a concatenação, o número será convertido em uma sequência que usa o caractere decimal padrão do sistema e o Microsoft Access SQL aceita somente os caracteres decimais do padrão dos EUA.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como abrir uma propriedade Filter para determinar que registros incluir em um Recordset aberto subsequentemente.

**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```

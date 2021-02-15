---
title: Propriedade Field2.Expression (DAO)
TOCTitle: Expression Property
ms:assetid: 8ae9db2c-7460-5bfc-0dc4-3f87e5ab30ff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197109(v=office.15)
ms:contentKeyID: 48546205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 603dfaa9a54ddfe769b96a57b790b4657abbeb14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292815"
---
# <a name="field2expression-property-dao"></a>Propriedade Field2.Expression (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Obtém ou define uma expressão que representa a fórmula para um campo calculado. **String** de leitura/gravação.

## <a name="version-information"></a>Informação da versão

Versão adicionada: Access 2010

## <a name="syntax"></a>Sintaxe

*expressão* . Expressão

*expressão* Uma variável que representa um objeto **Field2**.

## <a name="remarks"></a>Comentários

No Access 2013, você pode criar campos de tabela que calculam valores. Os cálculos podem incluir valores de campos na mesma tabela, bem como funções do Access interno.

O cálculo não pode incluir campos de outras tabelas ou consultas.

Os resultados do cálculo são somente leitura.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como criar um item de lista. O método CreateField cria um campo denominado **NomeCompleto**. A propriedade de expressão, em seguida, está definida como a expressão que calcula o valor do campo.

**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```


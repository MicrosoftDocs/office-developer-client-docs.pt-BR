---
title: Propriedade index. Unique (DAO)
TOCTitle: Unique Property
ms:assetid: a4486da5-8a1a-b4fc-0e07-e65cd2e726f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821087(v=office.15)
ms:contentKeyID: 48546809
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052990
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5c94200245b4736ad244cb37beec617a98d6c367
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291689"
---
# <a name="indexunique-property-dao"></a>Propriedade index. Unique (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna um valor que indica se objeto **[Index](index-object-dao.md)** representa um índice (chave) exclusivo para uma tabela (somente em espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . Diferente

*expressão* Uma variável que representa um objeto **index** .

## <a name="remarks"></a>Comentários

Essa definição de propriedade será leitura/gravação até que objeto seja acrescentado a uma coleção; depois disso, será somente leitura.

Um índice exclusivo é composto de um ou vários campos que organizam, de forma lógica, todos os registros em uma tabela em uma ordem exclusiva e predefinida. Se o índice for composto de um campo, os valores desse campo deverão ser exclusivos para a tabela inteira. Se o índice for composto por mais de um campo, cada campo conterá os valores duplicados, mas cada combinação de valores de todos os campos indexados deverá ser exclusiva.

Se ambas as propriedades **Unique** e **[Primary](index-primary-property-dao.md)** de um objeto **Index** estiverem definidas como **True**, o índice será exclusivo e primário: identificará exclusivamente todos os registros da tabela em uma ordem lógica e predefinida. Se a propriedade **Primary** estiver definida como **False**, o índice será um índice secundário. Os índices secundários (ambos chave e não chave) organizam logicamente os registros em uma ordem predefinida sem servirem de identificadores para os registros de uma tabela.

> [!NOTE]
> - Não é necessário criar índices para tabelas mas, em tabelas grandes e não indexadas, o acesso a um registro específico pode demorar muito tempo.
> - Os registros recuperados das tabelas sem os índices não são retornados em uma sequência específica.
> - A propriedade **[Attributes](field-attributes-property-dao.md)** de cada objeto **[Field](field-object-dao.md)** no objeto **Index** determina a ordem dos registros e, consequentemente, determina as técnicas de acesso para uso desse objeto **Index**.
> - Um índice exclusivo ajuda a otimizar a localização de registros.
> - Os índices não afetam a ordem física de uma tabela base; os índices afetam apenas a forma como os registros são acessados pelo objeto **[Recordset](recordset-object-dao.md)** do tipo tabela quando um índice específico é escolhido ou quando o mecanismo de banco de dados do Microsoft Access cria objetos **Recordset** .

## <a name="example"></a>Exemplo

Este exemplo define a propriedade **Unique** de um novo objeto **Index** como **True** e acrescenta-o à coleção **Indexes** da tabela Funcionários. Em seguida, enumera a coleção **Indexes** da coleção **TableDef** e da coleção **Properties** de cada objeto **Index**. O novo objeto **Index** permitirá somente um registro com uma combinação específica de Country, LastName e FirstName no objeto **TableDef**.

```vb
    Sub UniqueX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfEmployees As TableDef 
       Dim idxNew As Index 
       Dim idxLoop As Index 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set tdfEmployees = dbsNorthwind!Employees 
     
       With tdfEmployees 
          ' Create and append new Index object to the Indexes  
          ' collection of the Employees table. 
          Set idxNew = .CreateIndex("NewIndex") 
     
          With idxNew 
             .Fields.Append .CreateField("Country") 
             .Fields.Append .CreateField("LastName") 
             .Fields.Append .CreateField("FirstName") 
             .Unique = True 
          End With 
     
          .Indexes.Append idxNew 
          .Indexes.Refresh 
     
          Debug.Print .Indexes.Count & " Indexes in " & _ 
             .Name & " TableDef" 
     
          ' Enumerate Indexes collection of Employees table. 
          For Each idxLoop In .Indexes 
             Debug.Print "  " & idxLoop.Name 
     
             ' Enumerate Properties collection of each Index  
             ' object. 
             For Each prpLoop In idxLoop.Properties 
                Debug.Print "    " & prpLoop.Name & _ 
                   " = " & IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          Next idxLoop 
     
          ' Delete new Index because this is a demonstration. 
          .Indexes.Delete idxNew.Name 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```

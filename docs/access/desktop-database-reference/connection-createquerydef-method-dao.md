---
title: Método Connection.CreateQueryDef (DAO)
TOCTitle: CreateQueryDef Method
ms:assetid: 254fe81a-9b45-e8e7-108d-503c1c1c0fcc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191860(v=office.15)
ms:contentKeyID: 48543781
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053067
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 35bf71742133b65c2e55583e1c62922cb5bc91e8
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606035"
---
# <a name="connectioncreatequerydef-method-dao"></a>Método Connection.CreateQueryDef (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Cria um novo objeto **[QueryDef](querydef-object-dao.md)**.

## <a name="syntax"></a>Sintaxe

*expressão* . CreateQueryDef (***Name***, ***SQLText***)

*expressão* Uma variável que representa um objeto de **Conexão** .

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
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um <strong>Variant</strong> (subtipo <strong>String</strong>) que denomina exclusivamente o novo <strong>QueryDef</strong>.</p></td>
</tr>
<tr class="even">
<td><p>SQLText</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um <strong>Variant</strong> (subtipo <strong>String</strong>) que é uma instrução SQL definindo o <strong>QueryDef</strong>. Se você omitir esse argumento, será possível definir o <strong>QueryDef</strong> configurando sua propriedade <strong><a href="querydef-sql-property-dao.md">SQL</a></strong> antes ou depois de acrescentá-lo a uma coleção.</p></td>
</tr>
</tbody>
</table>


<<<<<<< Cabeça
### <a name="return-value"></a>Valor retornado
=======
### <a name="return-value"></a>Valor de retorno
>>>>>>> mestre

QueryDef

## <a name="remarks"></a>Comentários

Em um espaço de trabalho do Microsoft Access, se você fornecer algo diferente de uma cadeia de caracteres de comprimento zero para o nome ao criar um **QueryDef**, o objeto **QueryDef** resultante será automaticamente acrescentado à coleção **[QueryDefs](querydefs-collection-dao.md)**.

Se o objeto especificado pelo nome, já é um membro da coleção **QueryDefs** , ocorrerá um erro de tempo de execução. Você pode criar um temporário **QueryDef** usando uma cadeia de caracteres de comprimento zero para o argumento nome quando você executar o método **CreateQueryDef** . Também é possível realizar isso configurando a propriedade **[Name](connection-name-property-dao.md)** de um **QueryDef** recém-criado como uma cadeia de caracteres de comprimento zero (""). Objetos **QueryDef** temporários são úteis se você desejar usar repetidamente instruções SQL dinâmicas sem ter de criar novos objetos permanentes na coleção **QueryDefs**. Não é possível acrescentar um **QueryDef** temporário a qualquer coleção porque uma cadeia de caracteres de comprimento zero não é um nome válido para um objeto **QueryDef** permanente. Sempre é possível definir as propriedades **Name** e **SQL** do objeto **QueryDef** recém-criado e subsequentemente acrescentar o **QueryDef** à coleção **QueryDefs**.

Para executar a instrução SQL em um objeto **QueryDef**, use o método **[Execute](connection-execute-method-dao.md)** ou **[OpenRecordset](connection-openrecordset-method-dao.md)**.

Usar um objeto **QueryDef** é a maneira preferencial de executar consultas passagem SQL com bancos de dados ODBC.

Para remover um objeto **QueryDef** de uma coleção **QueryDefs** em um banco de dados de mecanismo de banco de dados Microsoft Access, use o método **[Delete](fields-delete-method-dao.md)** na coleção.


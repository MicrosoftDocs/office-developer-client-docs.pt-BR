---
title: Método Index.CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: fc82b785-8768-b144-a2a4-c1f1798865a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837208(v=office.15)
ms:contentKeyID: 48548892
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a3723beee3907cc209951c3494a2bde2a4c17bfa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463038"
---
# <a name="indexcreatefield-method-dao"></a>Método Index.CreateField (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Cria um novo objeto **[Field](field-object-dao.md)** (espaços de trabalho do Microsoft Access apenas).

## <a name="syntax"></a>Sintaxe

*expressão* . CreateField (***nome***, ***tipo***, ***tamanho***)

*expressão* Uma variável que representa um objeto **Index** .

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
<td><p>Uma string que denomina exclusivamente o novo objeto <strong>Field</strong>. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter detalhes sobre nomes válidos de <strong>Field</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Tipo</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>O argumento não tem suporte neste objeto.</p></td>
</tr>
<tr class="odd">
<td><p>Size</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>O argumento não tem suporte neste objeto.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor retornado

Field

## <a name="remarks"></a>Comentários

Você pode usar o método **CreateField** para criar um novo campo, bem como especificar o nome, o tipo de dados e o tamanho do campo. Se omitir uma ou mais dessas partes opcionais quando usar **CreateField**, você poderá usar uma instrução de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto à coleção. Depois de acrescentar o novo objeto, você poderá alterar algumas, mas não todas as configurações de propriedade. Consulte os tópicos individuais de propriedade para obter mais informações.

Os argumentos de tipo e tamanho se aplicam somente aos objetos de **campo** em um objeto **TableDef** . Esses argumentos são ignorados quando um objeto **Field** é associado com um objeto **Index** ou **Relation**.

Se name fizer referência a um objeto que já é um membro da coleção, ocorrerá um erro de tempo de execução quando você usa o método **[Append](fields-append-method-dao.md)** .

Para remover um objeto **Field** de uma coleção **Fields**, use o método **[Delete](fields-delete-method-dao.md)** na coleção. Você não pode excluir um objeto **Field** de uma coleção **Fields** do objeto **TableDef** depois de criar um índice que faz referência ao campo.


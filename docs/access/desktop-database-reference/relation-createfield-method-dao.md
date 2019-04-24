---
title: Método relation. CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: bc60c91e-acef-1c90-7303-12f77cce15b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822717(v=office.15)
ms:contentKeyID: 48547411
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ae322277dd1d357aceb3f9129110dded705f9eca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307055"
---
# <a name="relationcreatefield-method-dao"></a>Método relation. CreateField (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Cria um novo objeto **[Field](field-object-dao.md)** (apenas espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . CreateField (***nome***, ***tipo***, ***tamanho***)

*expressão* Uma variável que representa um objeto **relation** .

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
<td><p><em>Nome</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma string que denomina exclusivamente o novo objeto <strong>Field</strong>. Consulte a propriedade <strong><a href="connection-name-property-dao.md">Name</a></strong> para obter detalhes sobre nomes de <strong>campo</strong> válidos.</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>O argumento não tem suporte neste objeto.</p></td>
</tr>
<tr class="odd">
<td><p><em>Size</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>O argumento não tem suporte neste objeto.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor de retorno

Campo

## <a name="remarks"></a>Comentários

Você pode usar o método **CreateField** para criar um novo campo, bem como especificar o nome, o tipo dos dados e o tamanho do campo. Se você omitir uma ou mais das partes opcionais ao utilizar **CreateField**, poderá usar uma instruções de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto a uma coleção. Depois de acrescentar o novo objeto, será possível alterar algumas, mas não todas as suas configurações de propriedade. Consulte os tópicos de propriedade individuais para obter mais detalhes.

Os argumentos Type e Size aplicam-se somente aos objetos **Field** em um objeto **TableDef** . Esses argumentos serão ignorados quando o objeto **Field** for associado a um objeto **Index** ou **Relation**.

Se Name se referir a um objeto que já é um membro da coleção, ocorrerá um erro em tempo de execução quando você usar o método **[Append](fields-append-method-dao.md)** .

Para remover um objeto **Field** de uma coleção **Fields**, use o método **[Delete](fields-delete-method-dao.md)** na coleção. Não é possível excluir um objeto **Field** de uma coleção **Fields** do objeto **TableDef** depois de criar um index que faça referência ao campo.


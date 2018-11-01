---
title: Propriedade Sort (ADO)
TOCTitle: Sort property (ADO)
ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15)
ms:contentKeyID: 48548652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ebd515d2812ce453711c2b6519b1875250911d1a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886603"
---
# <a name="sort-property-ado"></a>Propriedade Sort (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Indica um ou mais nomes de campo nos quais o [Recordset](recordset-object-ado.md) é classificado e se cada campo é classificado na ordem crescente ou decrescente.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **String** que indica os nomes dos campos do **Recordset** no qual classificá-los. Cada nome é separado por uma vírgula e é, opcionalmente, seguido por um espaço em branco e pela palavra-chave, **ASC**, que classifica o campo na ordem crescente ou **DESC**, que classifica o campo na ordem decrescente. Por padrão, se nenhuma palavra-chave for especificada, o campo será classificado na ordem crescente.

## <a name="remarks"></a>Comentários

Essa propriedade exige que a propriedade [CursorLocation](cursorlocation-property-ado.md) seja definida como **adUseClient**. Se ainda não existir um índice, será criado um temporário para cada campo especificado na propriedade **Sort**.

A operação de classificação é eficiente, pois os dados não são reorganizados fisicamente, mas simplesmente acessados na ordem especificada pelo índice.

A definição da propriedade **Sort** em uma sequência de caracteres vazia redefinirá as linhas para sua ordem original e excluirá os índices temporários. Os índices existentes não serão excluídos.

Suponha que um **Recordset** contém três campos chamado *"MiddleInitial"*, *firstName*e *lastName*. Definir a propriedade **Sort** à cadeia de caracteres, "Sobrenome DESC, firstName ASC", que será ordenar o **conjunto de registros** por sobrenome em ordem decrescente e, em seguida, por nome em ordem crescente. A inicial do segundo nome será ignorada.

Nenhum campo poderá ser nomeado como "ASC" ou "DESC", pois esses nomes entrariam em conflito com as palavras-chave **ASC** e **DESC**. Forneça um alias ao campo com um nome conflitante utilizando a palavra-chave **AS** na consulta que retornar o **Recordset**.


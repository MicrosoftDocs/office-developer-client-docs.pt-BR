---
title: Propriedades Unique Table, Unique Schema, Unique Catalog -- Dinâmicas (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog Properties--Dynamic (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cd21c8b7c71f5fe1c95d347758e486f3854efab0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462670"
---
# <a name="unique-table-unique-schema-unique-catalog-properties--dynamic-ado"></a>Propriedades Unique Table, Unique Schema, Unique Catalog -- Dinâmicas (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Permite que você controle de perto as modificações em um determinada tabela base de um [Recordset](recordset-object-ado.md) formado por uma operação JOIN em diversas tabelas base.

  - **Unique Table** especifica o nome da tabela base na qual atualizações, inserções e exclusões são permitidas.

  - **Unique Schema** especifica o *esquema* ou o nome do proprietário da tabela.

  - **Unique Catalog** especifica o *catálogo* ou o nome do banco de dados que contém a tabela.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **String** que é o nome de uma tabela, um esquema ou um catálogo.

## <a name="remarks"></a>Comentários

A tabela base desejada é identificada com exclusividade por seus nomes de catálogo, esquema e tabela. Quando a propriedade **Unique Table** está definida, os valores das propriedades **Unique Schema** ou **Unique Catalog** são usados para localizar a tabela base. Deseja-se, mas não é necessário, que uma das propriedades **Unique Schema** e **Unique Catalog**, ou ambas, seja definida antes da propriedade **Unique Table**.

A chave primária de **Unique Table** é tratada como a chave primária de todo o **Recordset**. Essa é a chave que será usada para qualquer método que exija uma chave primária.

Enquanto **Unique Table** estiver definida, o método [Delete](delete-method-ado-recordset.md) afetará apenas a tabela nomeada. Os métodos [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md) e [UpdateBatch](updatebatch-method-ado.md) afetam quaisquer tabelas base subjacentes do **Recordset**.

A **Unique Table** deve ser especificada antes da realização de qualquer ressincronização personalizada. Se **Unique Table** não tiver sido especificada, a propriedade [Resync Command](resync-command-property-dynamic-ado.md) não terá efeito algum.

Um erro em tempo de execução será o resultado se não for possível encontrar uma tabela base exclusiva.

Essas propriedades dinâmicas serão acrescentadas à coleção **Properties** do objeto [Recordset](properties-collection-ado.md) quando a propriedade [CursorLocation](cursorlocation-property-ado.md) for definida como **adUseClient**.


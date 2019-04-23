---
title: Propriedade Name (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c7021c6f97d1aaa9c82e65eab98a3259d6eb87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288648"
---
# <a name="name-property-adox"></a>Propriedade Name (ADOX)

**Aplica-se ao:** Access 2013, Office 2013

Indica o nome do objeto.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **String**.

## <a name="remarks"></a>Comentários

Os nomes não precisam ser exclusivos em uma coleção.

A propriedade **Name** é de leitura/gravação nos objetos [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md) e [User](user-object-adox.md). A propriedade **Name** é somente leitura nos objetos [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md) e [View](view-object-adox.md).

No caso de objetos de leitura/gravação (**Column**, **Group**, **Key**, **Index**, **Table** e **User**), o valor padrão é uma sequência de caracteres vazia ("").

> [!NOTE]
> - No caso de chaves, esta propriedade é somente leitura em objetos **Key** já acrescentados a uma coleção.
> - [!OBSERVAçãO] No caso de tabelas, essa propriedade é somente leitura em objetos **Table** já acrescentados a uma coleção.



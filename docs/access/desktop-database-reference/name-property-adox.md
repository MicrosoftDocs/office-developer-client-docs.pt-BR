---
title: Propriedade Name (ADOX)
TOCTitle: Name Property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eab0b4b21f68f4facbd6b642aff4df5a328caad8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883110"
---
# <a name="name-property-adox"></a>Propriedade Name (ADOX)


**Aplica-se a**: Access 2013, o Office 2013

Indica o nome do objeto.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **String**.

## <a name="remarks"></a>Comentários

Os nomes não precisam ser exclusivos em uma coleção.

A propriedade **Name** é de leitura/gravação nos objetos [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md) e [User](user-object-adox.md). A propriedade **Name** é somente leitura nos objetos [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md) e [View](view-object-adox.md).

No caso de objetos de leitura/gravação (**Column**, **Group**, **Key**, **Index**, **Table** e **User**), o valor padrão é uma sequência de caracteres vazia ("").


> [!NOTE]
> <P>[!OBSERVAçãO] No caso de chaves, esta propriedade é somente leitura em objetos <STRONG>Key</STRONG> já acrescentados a uma coleção.</P>




> [!NOTE]
> <P>[!OBSERVAçãO] No caso de tabelas, essa propriedade é somente leitura em objetos <STRONG>Table</STRONG> já acrescentados a uma coleção.</P>



---
title: Propriedade Attributes (ADOX)
TOCTitle: Attributes property (ADOX)
ms:assetid: d5227b10-4a9b-5a57-d5ab-bbdd3e89aa95
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250072(v=office.15)
ms:contentKeyID: 48547959
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d39f05ecac42d416456e107b5a084797e034a0c3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931152"
---
# <a name="attributes-property-adox"></a>Propriedade Attributes (ADOX)


**Aplica-se a**: Access 2013, o Office 2013

Descreve características da coluna.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **Long**. O valor especifica características da tabela representada pelo objeto [Column](column-object-adox.md) e pode ser uma combinação das constantes [ColumnAttributesEnum](columnattributesenum.md). O valor padrão é zero (0), que não é **adColFixed** nem **adColNullable**.


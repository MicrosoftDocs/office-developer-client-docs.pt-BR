---
title: Objeto View (referência do banco de dados da área de trabalho do Access)
TOCTitle: View object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b5d25a727233b5fda5627df8dff952003bbfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306045"
---
# <a name="view-object-adox"></a>Objeto View (ADOX)


**Aplica-se ao:** Access 2013, Office 2013

Representa um conjunto de registros filtrado ou uma tabela virtual. Quando usado em conjunto com objeto [Command](command-object-ado.md) do ADO, o objeto **View** pode ser usado para adicionar, excluir ou modificar modos de exibição.

## <a name="remarks"></a>Comentários

Um modo de exibição é uma tabela virtual criada a partir de outros modos de exibição ou tabelas de bancos de dados. O objeto **View** permite que você crie um modo de exibição sem ter de saber ou usar a sintaxe "CREATE VIEW" do provedor.

Com as propriedades de um objeto **View**, você pode:

  - Identificar o modo de exibição com a propriedade [Name](name-property-adox.md).

  - Especificar o objeto **Command** do ADO que pode ser usado para adicionar, excluir ou modificar modos de exibição com a propriedade [Command](command-property-adox.md).

  - Retornar informações de data com as propriedades [DateCreated](datecreated-property-adox.md) e [DateModified](datemodified-property-adox.md).


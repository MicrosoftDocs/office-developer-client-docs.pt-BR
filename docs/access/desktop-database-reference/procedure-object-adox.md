---
title: Objeto Procedure (ADOX)
TOCTitle: Procedure object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ad8f87aa78fbc05694fc53f0d4a55dce43315077
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726152"
---
# <a name="procedure-object-adox"></a>Objeto Procedure (ADOX)


**Aplica-se a**: Access 2013, o Office 2013

Representa um procedimento armazenado. Quando usado em conjunto com objeto [Command](command-object-ado.md) do ADO, o objeto **Procedure** pode ser empregado para adicionar, excluir ou modificar procedimentos armazenados.

## <a name="remarks"></a>Comentários

O objeto **Procedure** permite que você crie um procedimento armazenado sem ter de saber ou usar a sintaxe "CREATE PROCEDURE" do provedor.

Com as propriedades de um objeto **Procedure**, você pode:

  - Identificar o procedimento com a propriedade [Name](name-property-adox.md).

  - Especificar o objeto **Command** do ADO que pode ser usado para criar ou executar o procedimento com a propriedade [Command](command-property-adox.md).

  - Retornar informações de data com as propriedades [DateCreated](datecreated-property-adox.md) e [DateModified](datemodified-property-adox.md).


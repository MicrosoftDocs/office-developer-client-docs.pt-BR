---
title: Objeto Procedure (ADOX)
TOCTitle: Procedure Object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5363bd435a4950b833e110fdda4f14a9c1bc2bc2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465201"
---
# <a name="procedure-object-adox"></a>Objeto Procedure (ADOX)


**Aplica-se a**: Access 2013 | Office 2013

Representa um procedimento armazenado. Quando usado em conjunto com objeto [Command](command-object-ado.md) do ADO, o objeto **Procedure** pode ser empregado para adicionar, excluir ou modificar procedimentos armazenados.

## <a name="remarks"></a>Comentários

O objeto **Procedure** permite que você crie um procedimento armazenado sem ter de saber ou usar a sintaxe "CREATE PROCEDURE" do provedor.

Com as propriedades de um objeto **Procedure**, você pode:

  - Identificar o procedimento com a propriedade [Name](name-property-adox.md).

  - Especificar o objeto **Command** do ADO que pode ser usado para criar ou executar o procedimento com a propriedade [Command](command-property-adox.md).

  - Retornar informações de data com as propriedades [DateCreated](datecreated-property-adox.md) e [DateModified](datemodified-property-adox.md).


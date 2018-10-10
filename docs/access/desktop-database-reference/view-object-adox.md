---
title: Objeto View (ADOX - referência de banco de dados da área de trabalho do Access)
TOCTitle: View Object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca58dd83ee3d3675a4ca272e1074b8d8cc930391
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465255"
---
# <a name="view-object-adox"></a>Objeto View (ADOX)


**Aplica-se a**: Access 2013 | Office 2013

Representa um conjunto de registros filtrado ou uma tabela virtual. Quando usado em conjunto com objeto [Command](command-object-ado.md) do ADO, o objeto **View** pode ser usado para adicionar, excluir ou modificar modos de exibição.

## <a name="remarks"></a>Comentários

Um modo de exibição é uma tabela virtual criada a partir de outros modos de exibição ou tabelas de bancos de dados. O objeto **View** permite que você crie um modo de exibição sem ter de saber ou usar a sintaxe "CREATE VIEW" do provedor.

Com as propriedades de um objeto **View**, você pode:

  - Identificar o modo de exibição com a propriedade [Name](name-property-adox.md).

  - Especificar o objeto **Command** do ADO que pode ser usado para adicionar, excluir ou modificar modos de exibição com a propriedade [Command](command-property-adox.md).

  - Retornar informações de data com as propriedades [DateCreated](datecreated-property-adox.md) e [DateModified](datemodified-property-adox.md).


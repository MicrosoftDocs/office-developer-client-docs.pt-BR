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
# <a name="view-object-adox"></a><span data-ttu-id="894b3-102">Objeto View (ADOX)</span><span class="sxs-lookup"><span data-stu-id="894b3-102">View object (ADOX)</span></span>


<span data-ttu-id="894b3-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="894b3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="894b3-p101">Representa um conjunto de registros filtrado ou uma tabela virtual. Quando usado em conjunto com objeto [Command](command-object-ado.md) do ADO, o objeto **View** pode ser usado para adicionar, excluir ou modificar modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="894b3-p101">Represents a filtered set of records or a virtual table. When used in conjunction with the ADO [Command](command-object-ado.md) object, the **View** object can be used for adding, deleting, or modifying views.</span></span>

## <a name="remarks"></a><span data-ttu-id="894b3-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="894b3-106">Remarks</span></span>

<span data-ttu-id="894b3-p102">Um modo de exibição é uma tabela virtual criada a partir de outros modos de exibição ou tabelas de bancos de dados. O objeto **View** permite que você crie um modo de exibição sem ter de saber ou usar a sintaxe "CREATE VIEW" do provedor.</span><span class="sxs-lookup"><span data-stu-id="894b3-p102">A view is a virtual table, created from other database tables or views. The **View** object allows you to create a view without having to know or use the provider's "CREATE VIEW" syntax.</span></span>

<span data-ttu-id="894b3-109">Com as propriedades de um objeto **View**, você pode:</span><span class="sxs-lookup"><span data-stu-id="894b3-109">With the properties of a **View** object, you can:</span></span>

  - <span data-ttu-id="894b3-110">Identificar o modo de exibição com a propriedade [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="894b3-110">Identify the view with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="894b3-111">Especificar o objeto **Command** do ADO que pode ser usado para adicionar, excluir ou modificar modos de exibição com a propriedade [Command](command-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="894b3-111">Specify the ADO **Command** object that can be used to add, delete, or modify views with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="894b3-112">Retornar informações de data com as propriedades [DateCreated](datecreated-property-adox.md) e [DateModified](datemodified-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="894b3-112">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>


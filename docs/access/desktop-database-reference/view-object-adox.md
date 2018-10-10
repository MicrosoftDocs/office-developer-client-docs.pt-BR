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
# <a name="view-object-adox"></a><span data-ttu-id="17e55-102">Objeto View (ADOX)</span><span class="sxs-lookup"><span data-stu-id="17e55-102">View Object (ADOX)</span></span>


<span data-ttu-id="17e55-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="17e55-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="17e55-p101">Representa um conjunto de registros filtrado ou uma tabela virtual. Quando usado em conjunto com objeto [Command](command-object-ado.md) do ADO, o objeto **View** pode ser usado para adicionar, excluir ou modificar modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="17e55-p101">Represents a filtered set of records or a virtual table. When used in conjunction with the ADO [Command](command-object-ado.md) object, the **View** object can be used for adding, deleting, or modifying views.</span></span>

## <a name="remarks"></a><span data-ttu-id="17e55-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="17e55-106">Remarks</span></span>

<span data-ttu-id="17e55-p102">Um modo de exibição é uma tabela virtual criada a partir de outros modos de exibição ou tabelas de bancos de dados. O objeto **View** permite que você crie um modo de exibição sem ter de saber ou usar a sintaxe "CREATE VIEW" do provedor.</span><span class="sxs-lookup"><span data-stu-id="17e55-p102">A view is a virtual table, created from other database tables or views. The **View** object allows you to create a view without having to know or use the provider's "CREATE VIEW" syntax.</span></span>

<span data-ttu-id="17e55-109">Com as propriedades de um objeto **View**, você pode:</span><span class="sxs-lookup"><span data-stu-id="17e55-109">With the properties of a **View** object, you can:</span></span>

  - <span data-ttu-id="17e55-110">Identificar o modo de exibição com a propriedade [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="17e55-110">Identify the view with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="17e55-111">Especificar o objeto **Command** do ADO que pode ser usado para adicionar, excluir ou modificar modos de exibição com a propriedade [Command](command-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="17e55-111">Specify the ADO **Command** object that can be used to add, delete, or modify views with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="17e55-112">Retornar informações de data com as propriedades [DateCreated](datecreated-property-adox.md) e [DateModified](datemodified-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="17e55-112">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>


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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301390"
---
# <a name="procedure-object-adox"></a><span data-ttu-id="09761-102">Objeto Procedure (ADOX)</span><span class="sxs-lookup"><span data-stu-id="09761-102">Procedure object (ADOX)</span></span>


<span data-ttu-id="09761-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="09761-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09761-p101">Representa um procedimento armazenado. Quando usado em conjunto com objeto [Command](command-object-ado.md) do ADO, o objeto **Procedure** pode ser empregado para adicionar, excluir ou modificar procedimentos armazenados.</span><span class="sxs-lookup"><span data-stu-id="09761-p101">Represents a stored procedure. When used in conjunction with the ADO [Command](command-object-ado.md) object, the **Procedure** object can be used for adding, deleting, or modifying stored procedures.</span></span>

## <a name="remarks"></a><span data-ttu-id="09761-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="09761-106">Remarks</span></span>

<span data-ttu-id="09761-107">O objeto **Procedure** permite que você crie um procedimento armazenado sem ter de saber ou usar a sintaxe "CREATE PROCEDURE" do provedor.</span><span class="sxs-lookup"><span data-stu-id="09761-107">The **Procedure** object allows you to create a stored procedure without having to know or use the provider's "CREATE PROCEDURE" syntax.</span></span>

<span data-ttu-id="09761-108">Com as propriedades de um objeto **Procedure**, você pode:</span><span class="sxs-lookup"><span data-stu-id="09761-108">With the properties of a **Procedure** object, you can:</span></span>

  - <span data-ttu-id="09761-109">Identificar o procedimento com a propriedade [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="09761-109">Identify the procedure with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="09761-110">Especificar o objeto **Command** do ADO que pode ser usado para criar ou executar o procedimento com a propriedade [Command](command-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="09761-110">Specify the ADO **Command** object that can be used to create or execute the procedure with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="09761-111">Retornar informações de data com as propriedades [DateCreated](datecreated-property-adox.md) e [DateModified](datemodified-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="09761-111">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>


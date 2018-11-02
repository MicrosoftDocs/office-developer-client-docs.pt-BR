---
title: Objeto Procedure (ADOX)
TOCTitle: Procedure object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72f0475aeca38b5c6ba6cd2954ff894f00fb6f7f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922647"
---
# <a name="procedure-object-adox"></a><span data-ttu-id="0d716-102">Objeto Procedure (ADOX)</span><span class="sxs-lookup"><span data-stu-id="0d716-102">Procedure object (ADOX)</span></span>


<span data-ttu-id="0d716-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d716-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d716-p101">Representa um procedimento armazenado. Quando usado em conjunto com objeto [Command](command-object-ado.md) do ADO, o objeto **Procedure** pode ser empregado para adicionar, excluir ou modificar procedimentos armazenados.</span><span class="sxs-lookup"><span data-stu-id="0d716-p101">Represents a stored procedure. When used in conjunction with the ADO [Command](command-object-ado.md) object, the **Procedure** object can be used for adding, deleting, or modifying stored procedures.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d716-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d716-106">Remarks</span></span>

<span data-ttu-id="0d716-107">O objeto **Procedure** permite que você crie um procedimento armazenado sem ter de saber ou usar a sintaxe "CREATE PROCEDURE" do provedor.</span><span class="sxs-lookup"><span data-stu-id="0d716-107">The **Procedure** object allows you to create a stored procedure without having to know or use the provider's "CREATE PROCEDURE" syntax.</span></span>

<span data-ttu-id="0d716-108">Com as propriedades de um objeto **Procedure**, você pode:</span><span class="sxs-lookup"><span data-stu-id="0d716-108">With the properties of a **Procedure** object, you can:</span></span>

  - <span data-ttu-id="0d716-109">Identificar o procedimento com a propriedade [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0d716-109">Identify the procedure with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="0d716-110">Especificar o objeto **Command** do ADO que pode ser usado para criar ou executar o procedimento com a propriedade [Command](command-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0d716-110">Specify the ADO **Command** object that can be used to create or execute the procedure with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="0d716-111">Retornar informações de data com as propriedades [DateCreated](datecreated-property-adox.md) e [DateModified](datemodified-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="0d716-111">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>


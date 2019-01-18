---
title: Propriedade DefaultDatabase (ADO)
TOCTitle: DefaultDatabase property (ADO)
ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15)
ms:contentKeyID: 48546784
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 01ca42ff738afe3a35cab6263cdae32ac256f3d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702639"
---
# <a name="defaultdatabase-property-ado"></a><span data-ttu-id="7e334-102">Propriedade DefaultDatabase (ADO)</span><span class="sxs-lookup"><span data-stu-id="7e334-102">DefaultDatabase property (ADO)</span></span>


<span data-ttu-id="7e334-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e334-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e334-104">Indica o banco de dados padrão para um objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7e334-104">Indicates the default database for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7e334-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="7e334-105">Settings and return values</span></span>

<span data-ttu-id="7e334-106">Define ou retorna um valor **String** que avalia o nome de um banco de dados disponível no provedor.</span><span class="sxs-lookup"><span data-stu-id="7e334-106">Sets or returns a **String** value that evaluates to the name of a database available from the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e334-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e334-107">Remarks</span></span>

<span data-ttu-id="7e334-108">Use a propriedade **DefaultDatabase** para definir ou retornar o nome do banco de dados padrão em um objeto **Connection** específico.</span><span class="sxs-lookup"><span data-stu-id="7e334-108">Use the **DefaultDatabase** property to set or return the name of the default database on a specific **Connection** object.</span></span>

<span data-ttu-id="7e334-p101">Se houver um banco de dados padrão, as sequências SQL poderão usar uma sintaxe não qualificada para acessar objetos no banco de dados. Para acessar objetos em um banco de dados que não seja aquele especificado na propriedade **DefaultDatabase**, é preciso qualificar os nomes dos objetos com o nome do banco de dados desejado. Na conexão, o provedor gravará as informações do banco de dados padrão na propriedade **DefaultDatabase**. Alguns provedores permitem apenas um banco de dados por conexão, caso em que não é possível alterar a propriedade **DefaultDatabase**.</span><span class="sxs-lookup"><span data-stu-id="7e334-p101">If there is a default database, SQL strings may use an unqualified syntax to access objects in that database. To access objects in a database other than the one specified in the **DefaultDatabase** property, you must qualify object names with the desired database name. Upon connection, the provider will write default database information to the **DefaultDatabase** property. Some providers allow only one database per connection, in which case you cannot change the **DefaultDatabase** property.</span></span>

<span data-ttu-id="7e334-113">Algumas fontes de dados e provedores talvez não ofereçam suporte a esse recurso e podem retornar um erro ou uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="7e334-113">Some data sources and providers may not support this feature, and may return an error or an empty string.</span></span>

<span data-ttu-id="7e334-114">**Uso de serviço de dados remotos** Essa propriedade não está disponível em um objeto de **Conexão** do cliente.</span><span class="sxs-lookup"><span data-stu-id="7e334-114">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>


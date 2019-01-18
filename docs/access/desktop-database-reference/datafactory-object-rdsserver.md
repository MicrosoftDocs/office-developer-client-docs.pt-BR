---
title: Objeto DataFactory (RDSServer)
TOCTitle: DataFactory object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77cd06992ef0062859d0a1372d115f8e65246a5d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702177"
---
# <a name="datafactory-object-rdsserver"></a><span data-ttu-id="9aa94-102">Objeto DataFactory (RDSServer)</span><span class="sxs-lookup"><span data-stu-id="9aa94-102">DataFactory object (RDSServer)</span></span>


<span data-ttu-id="9aa94-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="9aa94-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9aa94-104">Este objeto corporativo padrão do servidor implementa os métodos que fornecem acesso de leitura/gravação aos dados das fontes de dados especificadas para os aplicativos do cliente.</span><span class="sxs-lookup"><span data-stu-id="9aa94-104">This default server-side business object implements methods that provide read/write data access to specified data sources for client-side applications.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aa94-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="9aa94-105">Remarks</span></span>

<span data-ttu-id="9aa94-106">O objeto **RDSServer.DataFactory** foi criado como um objeto Automation do servidor que recebe solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="9aa94-106">The **RDSServer.DataFactory** object is designed as a server-side Automation object that receives client requests.</span></span> <span data-ttu-id="9aa94-107">Em uma implementação de Internet, ele reside em um servidor web e é instanciado pelo componente ADISAPI.</span><span class="sxs-lookup"><span data-stu-id="9aa94-107">In an Internet implementation, it resides on a web server and is instantiated by the ADISAPI component.</span></span> <span data-ttu-id="9aa94-108">O objeto **RDSServer.DataFactory** fornece acesso de leitura e gravação às fontes de dados especificadas, mas não contém nenhuma validação ou regras comerciais lógicas.</span><span class="sxs-lookup"><span data-stu-id="9aa94-108">The **RDSServer.DataFactory** object provides read and write access to specified data sources, but doesn't contain any validation or business rules logic.</span></span>

<span data-ttu-id="9aa94-p102">Se você usar um método disponível em ambos os objetos **RDSServer.DataFactory** e [RDS.DataControl](datacontrol-object-rds.md), o RDS usará a versão **RDS.DataControl** por padrão. O padrão adotará um cenário de programação básico, no qual o **RDSServer.DataFactory** servirá como um objeto corporativo genérico do servidor.</span><span class="sxs-lookup"><span data-stu-id="9aa94-p102">If you use a method that is available in both the **RDSServer.DataFactory** and [RDS.DataControl](datacontrol-object-rds.md) objects, Remote Data Service uses the **RDS.DataControl** version by default. The default assumes a basic programming scenario, where the **RDSServer.DataFactory** serves as a generic server-side business object.</span></span>

<span data-ttu-id="9aa94-111">Se desejar que seu aplicativo web para lidar com tarefas específicas processamento do lado do servidor, você pode substituir o **Rdsserver** com um objeto corporativo personalizado.</span><span class="sxs-lookup"><span data-stu-id="9aa94-111">If you want your web application to handle task-specific server-side processing, you can replace the **RDSServer.DataFactory** with a custom business object.</span></span>

<span data-ttu-id="9aa94-p103">Crie os objetos corporativos do servidor que chamam os métodos **RDSServer.DataFactory**, como [Query](query-method-rds.md) e [CreateRecordset](createrecordset-method-rds.md). Isso será útil, caso você queira adicionar funcionalidade aos objetos corporativos, mas tire proveito das tecnologias RDS existentes.</span><span class="sxs-lookup"><span data-stu-id="9aa94-p103">You can create server-side business objects that call the **RDSServer.DataFactory** methods, such as [Query](query-method-rds.md) and [CreateRecordset](createrecordset-method-rds.md). This is helpful if you want to add functionality to your business objects, but take advantage of existing Remote Data Service technologies.</span></span>

<span data-ttu-id="9aa94-114">A ID de classe do objeto **RDSServer.DataFactory** é 9381D8F5-0288-11D0-9501-00AA00B911A5.</span><span class="sxs-lookup"><span data-stu-id="9aa94-114">The class ID for the **RDSServer.DataFactory** object is 9381D8F5-0288-11D0-9501-00AA00B911A5.</span></span>


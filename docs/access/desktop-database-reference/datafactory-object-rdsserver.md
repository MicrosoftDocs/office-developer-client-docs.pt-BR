---
title: Objeto DataFactory (RDSServer)
TOCTitle: DataFactory Object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2249ea154ac40b9114dd3dab8006a6d26539adff
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605657"
---
# <a name="datafactory-object-rdsserver"></a><span data-ttu-id="2cec0-102">Objeto DataFactory (RDSServer)</span><span class="sxs-lookup"><span data-stu-id="2cec0-102">DataFactory Object (RDSServer)</span></span>


<span data-ttu-id="2cec0-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2cec0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2cec0-104">Este objeto corporativo padrão do servidor implementa os métodos que fornecem acesso de leitura/gravação aos dados das fontes de dados especificadas para os aplicativos do cliente.</span><span class="sxs-lookup"><span data-stu-id="2cec0-104">This default server-side business object implements methods that provide read/write data access to specified data sources for client-side applications.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cec0-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="2cec0-105">Remarks</span></span>

<span data-ttu-id="2cec0-106"><<<<<<< Cabeça o objeto **Rdsserver** destina-se como um objeto de automação do lado do servidor que recebe as solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="2cec0-106"><<<<<<< HEAD The **RDSServer.DataFactory** object is designed as a server-side Automation object that receives client requests.</span></span> <span data-ttu-id="2cec0-107">Em uma implementação da Internet, reside em um servidor Web e é instanciado pelo componente ADISAPI.</span><span class="sxs-lookup"><span data-stu-id="2cec0-107">In an Internet implementation, it resides on a Web server and is instantiated by the ADISAPI component.</span></span> <span data-ttu-id="2cec0-108">O objeto **RDSServer.DataFactory** fornece acesso de leitura e gravação às fontes de dados especificadas, mas não contém nenhuma validação ou regras comerciais lógicas.</span><span class="sxs-lookup"><span data-stu-id="2cec0-108">The **RDSServer.DataFactory** object provides read and write access to specified data sources, but doesn't contain any validation or business rules logic.</span></span>

<span data-ttu-id="2cec0-p102">Se você usar um método disponível em ambos os objetos **RDSServer.DataFactory** e [RDS.DataControl](datacontrol-object-rds.md), o RDS usará a versão **RDS.DataControl** por padrão. O padrão adotará um cenário de programação básico, no qual o **RDSServer.DataFactory** servirá como um objeto corporativo genérico do servidor.</span><span class="sxs-lookup"><span data-stu-id="2cec0-p102">If you use a method that is available in both the **RDSServer.DataFactory** and [RDS.DataControl](datacontrol-object-rds.md) objects, Remote Data Service uses the **RDS.DataControl** version by default. The default assumes a basic programming scenario, where the **RDSServer.DataFactory** serves as a generic server-side business object.</span></span>

<a name="if-you-want-your-web-application-to-handle-task-specific-server-side-processing-you-can-replace-the-rdsserverdatafactory-with-a-custom-business-object"></a><span data-ttu-id="2cec0-111">Se você quiser que o aplicativo da Web trate o processamento de tarefas específicas do servidor, substitua o **RDSServer.DataFactory** por um objeto corporativo personalizado.</span><span class="sxs-lookup"><span data-stu-id="2cec0-111">If you want your Web application to handle task-specific server-side processing, you can replace the **RDSServer.DataFactory** with a custom business object.</span></span>
=======
<span data-ttu-id="2cec0-112">O objeto **RDSServer.DataFactory** foi criado como um objeto Automation do servidor que recebe solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="2cec0-112">The **RDSServer.DataFactory** object is designed as a server-side Automation object that receives client requests.</span></span> <span data-ttu-id="2cec0-113">Em uma implementação de Internet, ele reside em um servidor web e é instanciado pelo componente ADISAPI.</span><span class="sxs-lookup"><span data-stu-id="2cec0-113">In an Internet implementation, it resides on a web server and is instantiated by the ADISAPI component.</span></span> <span data-ttu-id="2cec0-114">O objeto **RDSServer.DataFactory** fornece acesso de leitura e gravação às fontes de dados especificadas, mas não contém nenhuma validação ou regras comerciais lógicas.</span><span class="sxs-lookup"><span data-stu-id="2cec0-114">The **RDSServer.DataFactory** object provides read and write access to specified data sources, but doesn't contain any validation or business rules logic.</span></span>

<span data-ttu-id="2cec0-p104">Se você usar um método disponível em ambos os objetos **RDSServer.DataFactory** e [RDS.DataControl](datacontrol-object-rds.md), o RDS usará a versão **RDS.DataControl** por padrão. O padrão adotará um cenário de programação básico, no qual o **RDSServer.DataFactory** servirá como um objeto corporativo genérico do servidor.</span><span class="sxs-lookup"><span data-stu-id="2cec0-p104">If you use a method that is available in both the **RDSServer.DataFactory** and [RDS.DataControl](datacontrol-object-rds.md) objects, Remote Data Service uses the **RDS.DataControl** version by default. The default assumes a basic programming scenario, where the **RDSServer.DataFactory** serves as a generic server-side business object.</span></span>

<span data-ttu-id="2cec0-117">Se desejar que seu aplicativo web para lidar com tarefas específicas processamento do lado do servidor, você pode substituir o **Rdsserver** com um objeto corporativo personalizado.</span><span class="sxs-lookup"><span data-stu-id="2cec0-117">If you want your web application to handle task-specific server-side processing, you can replace the **RDSServer.DataFactory** with a custom business object.</span></span>
>>>>>>> <span data-ttu-id="2cec0-118">mestre</span><span class="sxs-lookup"><span data-stu-id="2cec0-118">master</span></span>

<span data-ttu-id="2cec0-p105">Crie os objetos corporativos do servidor que chamam os métodos **RDSServer.DataFactory**, como [Query](query-method-rds.md) e [CreateRecordset](createrecordset-method-rds.md). Isso será útil, caso você queira adicionar funcionalidade aos objetos corporativos, mas tire proveito das tecnologias RDS existentes.</span><span class="sxs-lookup"><span data-stu-id="2cec0-p105">You can create server-side business objects that call the **RDSServer.DataFactory** methods, such as [Query](query-method-rds.md) and [CreateRecordset](createrecordset-method-rds.md). This is helpful if you want to add functionality to your business objects, but take advantage of existing Remote Data Service technologies.</span></span>

<span data-ttu-id="2cec0-121">A ID de classe do objeto **RDSServer.DataFactory** é 9381D8F5-0288-11D0-9501-00AA00B911A5.</span><span class="sxs-lookup"><span data-stu-id="2cec0-121">The class ID for the **RDSServer.DataFactory** object is 9381D8F5-0288-11D0-9501-00AA00B911A5.</span></span>


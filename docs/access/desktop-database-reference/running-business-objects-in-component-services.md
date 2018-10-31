---
title: Executando objetos de negócios em serviços de componente
TOCTitle: Running Business Objects in Component Services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0eb70a615f49ff351ec31a826abc9775558218dd
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862552"
---
# <a name="running-business-objects-in-component-services"></a><span data-ttu-id="8ce29-102">Executando objetos de negócios em serviços de componente</span><span class="sxs-lookup"><span data-stu-id="8ce29-102">Running Business Objects in Component Services</span></span>


<span data-ttu-id="8ce29-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ce29-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8ce29-p101">Os objetos de negócios podem ser arquivos executáveis (.exe) ou bibliotecas de link dinâmico (.dll). A configuração que você usa para executar o objeto de negócios depende de o objeto ser um arquivo .dll ou .exe:</span><span class="sxs-lookup"><span data-stu-id="8ce29-p101">Business objects can be executable files (.exe) or dynamic-link libraries (.dll). The configuration you use to run the business object depends on whether the object is a .dll or .exe file:</span></span>

  - <span data-ttu-id="8ce29-p102">Os objetos de negócios criados como arquivos .exe podem ser chamados através do DCOM. Se esses objetos de negócios forem utilizados através do IIS (Internet Information Services), eles estarão sujeitos ao preparativo adicional de dados, que retardará o desempenho do cliente.</span><span class="sxs-lookup"><span data-stu-id="8ce29-p102">Business objects created as .exe files can be called through DCOM. If these business objects are used through Internet Information Services (IIS), they are subject to additional marshalingof data, which will slow client performance.</span></span>

  - <span data-ttu-id="8ce29-p103">Os objetos de negócios criados como arquivos .dll podem ser utilizados através do IIS (e portanto do HTTP). Eles também podem ser utilizados sobre o DCOM apenas através dos Component Services (ou Microsoft Transaction Server, se você estiver usando o Windows NT). As DLLs do objeto de negócios precisarão estar registradas no computador servidor IIS para fornecer a você acessibilidade através do IIS. (Para obter as etapas sobre como configurar uma DLL a ser executada no DCOM, consulte a seção, "[Ativando um DLL para executar no DCOM](enabling-a-dll-to-run-on-dcom.md).")</span><span class="sxs-lookup"><span data-stu-id="8ce29-p103">Business objects created as .dll files can be used via IIS (and therefore HTTP). They can also be used over DCOM only via Component Services (or Microsoft Transaction Server, if you are using Windows NT). Business object DLLs will need to be registered on the IIS server computer to give you accessibility via IIS. (For steps on how to configure a DLL to run on DCOM, see the section, "[Enabling a DLL to Run on DCOM](enabling-a-dll-to-run-on-dcom.md).")</span></span>


> [!NOTE]
> <span data-ttu-id="8ce29-112">Quando objetos corporativos na camada intermediária são implementados como componentes de serviços de componentes (usando **GetObjectContext**, **SetComplete**e **SetAbort**), eles podem usar os serviços de componentes (ou MTS, se você estiver usando o Windows NT) para os objetos de contexto manter seu estado entre várias chamadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="8ce29-112">When business objects on the middle tier are implemented as Component Services components (using **GetObjectContext**, **SetComplete**, and **SetAbort**), they can use Component Services (or MTS, if you are using Windows NT) context objects to maintain their state across multiple client calls.</span></span> <span data-ttu-id="8ce29-113">Esse cenário é possível com o DCOM, que geralmente é implementado entre os clientes e os servidores confiáveis (uma intranet).</span><span class="sxs-lookup"><span data-stu-id="8ce29-113">This scenario is possible with DCOM, which is typically implemented between trusted clients and servers (an intranet).</span></span> 
>
> <span data-ttu-id="8ce29-114">Nesse caso, o objeto [RDS.DataSpace](dataspace-object-rds.md) e o método [CreateObject](createobject-method-rds.md) na parte do cliente são substituídos pelo objeto de contexto de transação e o método **CreateInstance** (fornecidos pela interface **ITransactionContext** ) implementados pelos Component Services.</span><span class="sxs-lookup"><span data-stu-id="8ce29-114">In this case, the [RDS.DataSpace](dataspace-object-rds.md) object and [CreateObject](createobject-method-rds.md) method on the client side are replaced by the transaction context object and **CreateInstance** method (provided by the **ITransactionContext** interface), implemented by Component Services.</span></span>


## <a name="see-also"></a><span data-ttu-id="8ce29-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ce29-115">See also</span></span>

- [<span data-ttu-id="8ce29-116">Executar objetos corporativos nos serviços de componentes (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="8ce29-116">Running Business Objects in Component Services (SQL Server)</span></span>](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)
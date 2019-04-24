---
title: Execução de objetos Business em serviços de componente
TOCTitle: Running business objects in component services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23cb90161e5e0728aa652ae5d496216676f781a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309200"
---
# <a name="running-business-objects-in-component-services"></a><span data-ttu-id="51e31-102">Execução de objetos Business em serviços de componente</span><span class="sxs-lookup"><span data-stu-id="51e31-102">Running business objects in component services</span></span>

<span data-ttu-id="51e31-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51e31-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51e31-p101">Os objetos de negócios podem ser arquivos executáveis (.exe) ou bibliotecas de link dinâmico (.dll). A configuração que você usa para executar o objeto de negócios depende de o objeto ser um arquivo .dll ou .exe:</span><span class="sxs-lookup"><span data-stu-id="51e31-p101">Business objects can be executable files (.exe) or dynamic-link libraries (.dll). The configuration you use to run the business object depends on whether the object is a .dll or .exe file:</span></span>

- <span data-ttu-id="51e31-p102">Os objetos de negócios criados como arquivos .exe podem ser chamados através do DCOM. Se esses objetos de negócios forem utilizados através do IIS (Internet Information Services), eles estarão sujeitos ao preparativo adicional de dados, que retardará o desempenho do cliente.</span><span class="sxs-lookup"><span data-stu-id="51e31-p102">Business objects created as .exe files can be called through DCOM. If these business objects are used through Internet Information Services (IIS), they are subject to additional marshalingof data, which will slow client performance.</span></span>

- <span data-ttu-id="51e31-p103">Os objetos de negócios criados como arquivos .dll podem ser utilizados através do IIS (e portanto do HTTP). Eles também podem ser utilizados sobre o DCOM apenas através dos Component Services (ou Microsoft Transaction Server, se você estiver usando o Windows NT). As DLLs do objeto de negócios precisarão estar registradas no computador servidor IIS para fornecer a você acessibilidade através do IIS. (Para obter as etapas sobre como configurar uma DLL a ser executada no DCOM, consulte a seção, "[Ativando um DLL para executar no DCOM](enabling-a-dll-to-run-on-dcom.md).")</span><span class="sxs-lookup"><span data-stu-id="51e31-p103">Business objects created as .dll files can be used via IIS (and therefore HTTP). They can also be used over DCOM only via Component Services (or Microsoft Transaction Server, if you are using Windows NT). Business object DLLs will need to be registered on the IIS server computer to give you accessibility via IIS. (For steps on how to configure a DLL to run on DCOM, see the section, "[Enabling a DLL to Run on DCOM](enabling-a-dll-to-run-on-dcom.md).")</span></span>


> [!NOTE]
> <span data-ttu-id="51e31-112">Quando os objetos de negócios na camada intermediária são implementados como componentes de serviços \*\*\*\* de componente (usando getObjectContext, SetComplete e SetAbort), eles podem usar os serviços de componente (ou MTS, se você estiver usando o Windows NT) objetos de contexto para \*\*\*\* \*\*\*\* manter o estado entre várias chamadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="51e31-112">When business objects on the middle tier are implemented as Component Services components (using **GetObjectContext**, **SetComplete**, and **SetAbort**), they can use Component Services (or MTS, if you are using Windows NT) context objects to maintain their state across multiple client calls.</span></span> <span data-ttu-id="51e31-113">Esse cenário é possível com o DCOM, que geralmente é implementado entre os clientes e os servidores confiáveis (uma intranet).</span><span class="sxs-lookup"><span data-stu-id="51e31-113">This scenario is possible with DCOM, which is typically implemented between trusted clients and servers (an intranet).</span></span> 
>
> <span data-ttu-id="51e31-114">Nesse caso, o objeto [RDS.DataSpace](dataspace-object-rds.md) e o método [CreateObject](createobject-method-rds.md) na parte do cliente são substituídos pelo objeto de contexto de transação e o método **CreateInstance** (fornecidos pela interface **ITransactionContext** ) implementados pelos Component Services.</span><span class="sxs-lookup"><span data-stu-id="51e31-114">In this case, the [RDS.DataSpace](dataspace-object-rds.md) object and [CreateObject](createobject-method-rds.md) method on the client side are replaced by the transaction context object and **CreateInstance** method (provided by the **ITransactionContext** interface), implemented by Component Services.</span></span>


## <a name="see-also"></a><span data-ttu-id="51e31-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="51e31-115">See also</span></span>

- [<span data-ttu-id="51e31-116">Executando objetos de negócios nos serviços de componente (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="51e31-116">Running Business Objects in Component Services (SQL Server)</span></span>](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)

---
title: Especificação de threads por processador no IIS
TOCTitle: Specifying threads per processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 57e4b6228588af7f0d58caf53d3e093e824c7854
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308586"
---
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="90825-102">Especificação de threads por processador no IIS</span><span class="sxs-lookup"><span data-stu-id="90825-102">Specifying threads per processor on IIS</span></span>


<span data-ttu-id="90825-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="90825-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90825-104">Ao usar o RDS com o Internet Information Services 4.0 ou posterior, o número de threads criados por processador pode ser controlado manipulando o Registro no servidor Web.</span><span class="sxs-lookup"><span data-stu-id="90825-104">When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the web server.</span></span> <span data-ttu-id="90825-105">O número de encadeamentos por processador pode afetar o desempenho em uma situação de alto tráfego ou em situações de baixo tráfego em consultas de maior tamanho.</span><span class="sxs-lookup"><span data-stu-id="90825-105">The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes.</span></span> <span data-ttu-id="90825-106">O usuário deve experimentar para melhores resultados.</span><span class="sxs-lookup"><span data-stu-id="90825-106">The user should experiment for best results.</span></span>

<span data-ttu-id="90825-107">O método usado para determinar e alterar o valor padrão para essa definição depende da configuração do servidor IIS 4.0.</span><span class="sxs-lookup"><span data-stu-id="90825-107">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="90825-p102">Com o MDAC 2.1.2.4202.3 (GA) ou posterior instalado no IIS, o RDS usa o mesmo pool de encadeamento Component Services (ou Microsoft Transaction Services, se você estiver usando o Windows NT) usado pelos scripts ASP. O valor padrão para o número de encadeamentos por processador é 10. Para alterar o padrão, você deve incluir a seguinte chave para o registro do servidor:</span><span class="sxs-lookup"><span data-stu-id="90825-p102">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use. The default value for the number of threads per processor is 10. To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="90825-111">onde *MaxPoolThreads* é um REG \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="90825-111">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="90825-112">*MaxPoolThreads* não aparece no Registro, a menos que seja especificamente adicionado.</span><span class="sxs-lookup"><span data-stu-id="90825-112">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="90825-113">Os valores válidos variam de 5 a um máximo recomendado de 20.</span><span class="sxs-lookup"><span data-stu-id="90825-113">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="90825-114">Se o valor especificado pela chave de registro for superior ao valor da chave *PoolThreadLimit* (localizada no mesmo caminho), será usado o valor *PoolThreadLimit*.</span><span class="sxs-lookup"><span data-stu-id="90825-114">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="90825-p104">Como alternativa, se o MDAC 2.1 2.1.1.3711.11 (GA) ou anterior estiver instalado no servidor IIS, o valor padrão para o número de encadeamentos por processador será 6. Para alterar o padrão, você deve incluir a seguinte chave no registro do servidor IIS:</span><span class="sxs-lookup"><span data-stu-id="90825-p104">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6. To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="90825-117">onde *ADCThreads* é um REG \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="90825-117">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="90825-118">O *ADCThreads* não aparece no Registro a menos que seja especificamente adicionado.</span><span class="sxs-lookup"><span data-stu-id="90825-118">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="90825-119">O intervalo de valores válidos é de 1 a 50.</span><span class="sxs-lookup"><span data-stu-id="90825-119">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="90825-120">Se o valor especificado pela chave de registro for superior a 50, o valor máximo será usado (50).</span><span class="sxs-lookup"><span data-stu-id="90825-120">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>


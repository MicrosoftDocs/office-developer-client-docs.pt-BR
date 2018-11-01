---
title: Especificando encadeamentos por processador no IIS
TOCTitle: Specifying Threads Per Processor on IIS
ms:assetid: 12889d7b-5415-8077-2ca0-1c3a96fb89ec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248898(v=office.15)
ms:contentKeyID: 48543344
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4212b1c2bcf89badedbc7a3b7d4dc72a879a95c7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871980"
---
# <a name="specifying-threads-per-processor-on-iis"></a><span data-ttu-id="40ad0-102">Especificando encadeamentos por processador no IIS</span><span class="sxs-lookup"><span data-stu-id="40ad0-102">Specifying Threads Per Processor on IIS</span></span>


<span data-ttu-id="40ad0-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="40ad0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="40ad0-104">Ao usar o RDS com o Internet Information Services 4.0 ou posterior, o número de threads criados por processador pode ser controlado por manipulando o registro no servidor web.</span><span class="sxs-lookup"><span data-stu-id="40ad0-104">When using RDS with Internet Information Services 4.0 or later, the number of threads created per processor can be controlled by manipulating the registry on the web server.</span></span> <span data-ttu-id="40ad0-105">O número de encadeamentos por processador pode afetar o desempenho em uma situação de alto tráfego ou em situações de baixo tráfego em consultas de maior tamanho.</span><span class="sxs-lookup"><span data-stu-id="40ad0-105">The number of threads per processor can affect performance in a high traffic situation, or in low traffic situations with large query sizes.</span></span> <span data-ttu-id="40ad0-106">O usuário deve experimentar para melhores resultados.</span><span class="sxs-lookup"><span data-stu-id="40ad0-106">The user should experiment for best results.</span></span>

<span data-ttu-id="40ad0-107">O método usado para determinar e alterar o valor padrão para essa definição depende da configuração do servidor IIS 4.0.</span><span class="sxs-lookup"><span data-stu-id="40ad0-107">The method used to determine and change the default value for this setting depends upon the configuration of the IIS 4.0 server.</span></span>

<span data-ttu-id="40ad0-p102">Com o MDAC 2.1.2.4202.3 (GA) ou posterior instalado no IIS, o RDS usa o mesmo pool de encadeamento Component Services (ou Microsoft Transaction Services, se você estiver usando o Windows NT) usado pelos scripts ASP. O valor padrão para o número de encadeamentos por processador é 10. Para alterar o padrão, você deve incluir a seguinte chave para o registro do servidor:</span><span class="sxs-lookup"><span data-stu-id="40ad0-p102">With MDAC 2.1.2.4202.3 (GA) or later installed on the IIS server, RDS uses the same Component Services (or Microsoft Transaction Services, if you are using Windows NT) thread pool as ASP scripts use. The default value for the number of threads per processor is 10. To change the default, you must add the following key to the server registry:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\InetInfo\Parameters\MaxPoolThreads
```

<span data-ttu-id="40ad0-111">onde *MaxPoolThreads* é um REG\_DWORD.</span><span class="sxs-lookup"><span data-stu-id="40ad0-111">where *MaxPoolThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="40ad0-112">*MaxPoolThreads* não aparece no registro, a menos que especificamente, ela será adicionada.</span><span class="sxs-lookup"><span data-stu-id="40ad0-112">*MaxPoolThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="40ad0-113">Os valores válidos variam de 5 a um máximo recomendado de 20.</span><span class="sxs-lookup"><span data-stu-id="40ad0-113">Valid values range from 5 to a recommended maximum of 20.</span></span> <span data-ttu-id="40ad0-114">Se o valor especificado pela chave do registro for maior que o valor da chave *PoolThreadLimit* (localizada sob o mesmo caminho), o valor de *PoolThreadLimit* é usado.</span><span class="sxs-lookup"><span data-stu-id="40ad0-114">If the value specified by the registry key is greater than the value of the *PoolThreadLimit* key (located under the same path), then *PoolThreadLimit* value is used.</span></span>

<span data-ttu-id="40ad0-p104">Como alternativa, se o MDAC 2.1 2.1.1.3711.11 (GA) ou anterior estiver instalado no servidor IIS, o valor padrão para o número de encadeamentos por processador será 6. Para alterar o padrão, você deve incluir a seguinte chave no registro do servidor IIS:</span><span class="sxs-lookup"><span data-stu-id="40ad0-p104">Alternatively, if MDAC 2.1 2.1.1.3711.11 (GA) or earlier is installed on the IIS server, the default value for the number of threads per processor is 6. To change the default, you must add the following key to the registry on the IIS server:</span></span>

```vb 
 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\W3SVC\Parameters\ADCThreads
```

<span data-ttu-id="40ad0-117">onde *ADCThreads* é um registro\_DWORD.</span><span class="sxs-lookup"><span data-stu-id="40ad0-117">where *ADCThreads* is a REG\_DWORD.</span></span> <span data-ttu-id="40ad0-118">*ADCThreads* não aparece no registro, a menos que especificamente, ela será adicionada.</span><span class="sxs-lookup"><span data-stu-id="40ad0-118">*ADCThreads* does not appear in the Registry unless it is specifically added.</span></span> <span data-ttu-id="40ad0-119">O intervalo de valores válidos é de 1 a 50.</span><span class="sxs-lookup"><span data-stu-id="40ad0-119">The range of valid values is 1 to 50.</span></span> <span data-ttu-id="40ad0-120">Se o valor especificado pela chave de registro for superior a 50, o valor máximo será usado (50).</span><span class="sxs-lookup"><span data-stu-id="40ad0-120">If the value specified by the registry key is greater than 50, then the maximum value is used (50).</span></span>


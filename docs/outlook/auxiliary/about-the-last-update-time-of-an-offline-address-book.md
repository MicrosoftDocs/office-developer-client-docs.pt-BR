---
title: Sobre o último tempo de atualização de um catálogo de endereços offline
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d8c554c5-89ac-9b32-5561-8d8178d2525a
description: O OAB (Catálogo de Endereços Offline) oferece aos usuários do Outlook acesso em estado desconectado às informações de diretório da GAL (Lista de Endereços Globais) e de outras listas de endereços.
ms.openlocfilehash: 3374f87cd62d46a80ed823bff0516115a58c155c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317014"
---
# <a name="about-the-last-update-time-of-an-offline-address-book"></a><span data-ttu-id="b3b9f-103">Sobre o último tempo de atualização de um catálogo de endereços offline</span><span class="sxs-lookup"><span data-stu-id="b3b9f-103">About the last update time of an Offline Address Book</span></span>

<span data-ttu-id="b3b9f-104">O OAB (Catálogo de Endereços Offline) oferece aos usuários do Outlook acesso em estado desconectado às informações de diretório da GAL (Lista de Endereços Globais) e de outras listas de endereços.</span><span class="sxs-lookup"><span data-stu-id="b3b9f-104">An Offline Address Book (OAB) provides Outlook users in a disconnected state access to directory information from the Global Address List (GAL) and from other address books.</span></span> <span data-ttu-id="b3b9f-105">É uma cópia de um Catálogo de Endereços que o Outlook baixou de um servidor Exchange para fornecer acesso offline.</span><span class="sxs-lookup"><span data-stu-id="b3b9f-105">It is a copy of an Address Book that Outlook has downloaded from an Exchange server to provide offline access.</span></span>
  
<span data-ttu-id="b3b9f-106">Os administradores do Exchange podem escolher quais Catálogos de Endereços disponibilizar para os usuários que trabalham offline.</span><span class="sxs-lookup"><span data-stu-id="b3b9f-106">Exchange administrators can choose which Address Books to make available for users who work offline.</span></span> <span data-ttu-id="b3b9f-107">Para criar uma cópia de um Catálogo de Endereços, o Exchange gera novos arquivos OAB, compacta-os e coloca-os em um compartilhamento local.</span><span class="sxs-lookup"><span data-stu-id="b3b9f-107">To create a copy of an Address Book, Exchange generates new OAB files, compresses the files, and places them on a local share.</span></span> <span data-ttu-id="b3b9f-108">Dependendo da configuração do Outlook, o Outlook baixa os arquivos OAB da Web ou de uma Pasta Pública em um computador cliente para usar no estado desconectado.</span><span class="sxs-lookup"><span data-stu-id="b3b9f-108">Depending on how Outlook is configured, Outlook downloads the OAB files either from the Web or from a Public Folder to a client computer for use in a disconnected state.</span></span> <span data-ttu-id="b3b9f-109">O Outlook verifica periodicamente e baixa atualizações do OAB.</span><span class="sxs-lookup"><span data-stu-id="b3b9f-109">Outlook periodically checks for and downloads OAB updates.</span></span>
  
<span data-ttu-id="b3b9f-110">Soluções do Outlook que querem proporcionar aos usuários acesso offline a um OAB podem precisar descobrir quando o OAB foi atualizado pela última vez do servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="b3b9f-110">Outlook solutions that want to provide their users offline access to an OAB may need to find out when the OAB was last updated from the Exchange server.</span></span> <span data-ttu-id="b3b9f-111">Para localizar a hora da última atualização de um OAB, as soluções podem usar a entrada a seguir no registro do Windows: **HKCU\Software\Microsoft\Exchange\Exchange Provider\OAB Last Modified Time**.</span><span class="sxs-lookup"><span data-stu-id="b3b9f-111">To find the last update time of an OAB, solutions can use the following entry in the Windows registry: **HKCU\Software\Microsoft\Exchange\Exchange Provider\OAB Last Modified Time**.</span></span> <span data-ttu-id="b3b9f-112">O tipo desta entrada do registro é **REG_BINARY**.</span><span class="sxs-lookup"><span data-stu-id="b3b9f-112">The type of this registry entry is **REG_BINARY**.</span></span> <span data-ttu-id="b3b9f-113">Os dados têm 8 bytes de tamanho.</span><span class="sxs-lookup"><span data-stu-id="b3b9f-113">The data is 8 bytes in size.</span></span> <span data-ttu-id="b3b9f-114">Você pode converter os dados para uma estrutura [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) de 64 bits especificando o valor do Tempo Universal Coordenado (UTC) no qual o Outlook baixou os arquivos OAB do servidor Exchange pela última vez para o computador cliente.</span><span class="sxs-lookup"><span data-stu-id="b3b9f-114">You can convert the data to a 64-bit [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) structure specifying a Universal Coordinated Time (UTC) value that Outlook last downloaded the OAB files from the Exchange server to the client computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b3b9f-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3b9f-115">See also</span></span>

- [<span data-ttu-id="b3b9f-116">Gerenciar Catálogos de Endereços Offline</span><span class="sxs-lookup"><span data-stu-id="b3b9f-116">Managing Offline Address Books</span></span>](https://msdn.microsoft.com/library/b7f26eca-b93b-4834-ba50-11febdefbb18.aspx)


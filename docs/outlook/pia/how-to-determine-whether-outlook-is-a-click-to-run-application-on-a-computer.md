---
title: Determinar se o Outlook é um aplicativo Clique para Executar em um computador
TOCTitle: Determine whether Outlook is a Click-to-Run application on a computer
ms:assetid: 1b8573be-8ea8-4973-869d-87fda57ce525
ms:mtpsurl: https://msdn.microsoft.com/library/Ff522355(v=office.15)
ms:contentKeyID: 55119804
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a710baa4d70ac69b67d2a06fe694998884fd835
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356403"
---
# <a name="determine-whether-outlook-is-a-click-to-run-application-on-a-computer"></a><span data-ttu-id="46404-102">Determinar se o Outlook é um aplicativo Clique para Executar em um computador</span><span class="sxs-lookup"><span data-stu-id="46404-102">Determine whether Outlook is a Click-to-Run application on a computer</span></span>

<span data-ttu-id="46404-103">Clique para Executar é um mecanismo de distribuição e atualização de software disponível para o Office 2010 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="46404-103">Click-to-Run is a software delivery and updating mechanism available to Office 2010 and later versions.</span></span> <span data-ttu-id="46404-104">Produtos fornecidos por meio de Clique para Executar em um ambiente virtual de aplicativo no sistema operacional local.</span><span class="sxs-lookup"><span data-stu-id="46404-104">Products delivered via Click-to-Run execute in a virtual application environment on the local operating system.</span></span> <span data-ttu-id="46404-105">Isso significa que eles têm particulares cópias de seus arquivos e configurações, e as alterações que fazem são capturadas no ambiente virtual.</span><span class="sxs-lookup"><span data-stu-id="46404-105">This means that they have private copies of their files and settings, and that any changes they make are captured in the virtual environment.</span></span>

<span data-ttu-id="46404-106">O Clique para Executar é rápido: os usuários podem começar a executar um aplicativo em pouco tempo, sem ter que esperar que o produto completo conclua a instalação.</span><span class="sxs-lookup"><span data-stu-id="46404-106">Click-to-Run is fast—users can start running an application within a short time without waiting for the complete product to finish installing.</span></span> <span data-ttu-id="46404-107">As atualizações são executadas automaticamente em segundo plano, sem precisar que um usuário primeiro remova uma instalação ou instale as atualizações manualmente.</span><span class="sxs-lookup"><span data-stu-id="46404-107">Updates are run automatically in the background, without requiring a user to first remove an installation or manually install updates.</span></span> <span data-ttu-id="46404-108">Produtos Clique para Executar são virtualizados e não entram em conflito com outro software instalado.</span><span class="sxs-lookup"><span data-stu-id="46404-108">Click-to-Run products are virtualized and do not conflict with other installed software.</span></span> <span data-ttu-id="46404-109">No entanto, como um produto Clique para Executar tem cópias particulares de todos os respectivos arquivos e registros, um desenvolvedor de suplemento não consegue determinar a existência do produto da mesma forma que um produto instalado no disco rígido do computador do cliente.</span><span class="sxs-lookup"><span data-stu-id="46404-109">However, because a product delivered by Click-to-Run has private copies of all its files and registration, an add-in developer cannot determine the product’s existence in the same manner as a product that was installed on a client computer’s hard disk.</span></span> <span data-ttu-id="46404-110">Desde o Outlook 2010, os desenvolvedores de suplementos devem verificar se o Outlook está instalado e se o Outlook foi entregue como um produto Clique para Executar.</span><span class="sxs-lookup"><span data-stu-id="46404-110">Starting with Outlook 2010, add-in developers should verify whether Outlook has been installed, and whether Outlook has been delivered as a Click-to-Run product.</span></span>


> [!NOTE]
> <span data-ttu-id="46404-111">Somente o Office 2013 de 32 bits tem suporte para o ambiente virtual de aplicativos Clique para Executar, mesmo se o computador cliente usar um sistema operacional de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="46404-111">Only 32-bit Office 2013 is supported in the Click-to-Run virtual application environment, even if the client computer runs a 64-bit operating system.</span></span>



### <a name="to-check-whether-outlook-2013-was-delivered-by-click-to-run-on-a-client-computer"></a><span data-ttu-id="46404-112">Para verificar se o Outlook 2013 foi entregue pelo Clique para Executar em um computador cliente</span><span class="sxs-lookup"><span data-stu-id="46404-112">To check whether Outlook 2013 was delivered by Click-to-Run on a client computer</span></span>

- <span data-ttu-id="46404-113">Verifique se a chave VirtualOutlook existe no seguinte local no registro do Windows:</span><span class="sxs-lookup"><span data-stu-id="46404-113">Verify whether the VirtualOutlook key exists in the following location in the Windows registry:</span></span>
    
  `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
    
  <span data-ttu-id="46404-114">A chave VirtualOutlook é um valor REG\_SZ que contém a marca de cultura do idioma de produto instalado, como "pt-br".</span><span class="sxs-lookup"><span data-stu-id="46404-114">The VirtualOutlook key is a REG\_SZ value that contains the culture tag of the installed product language, such as "en-us".</span></span>

## <a name="see-also"></a><span data-ttu-id="46404-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="46404-115">See also</span></span>

- [<span data-ttu-id="46404-116">Suplemento de administração</span><span class="sxs-lookup"><span data-stu-id="46404-116">Add-in administration</span></span>](add-in-administration.md)


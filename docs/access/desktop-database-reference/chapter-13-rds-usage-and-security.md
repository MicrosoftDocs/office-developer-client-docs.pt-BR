---
title: 'Capítulo 13: Segurança e o uso do RDS'
TOCTitle: 'Chapter 13: RDS usage and security'
ms:assetid: 78add8bb-f01a-2efb-33f0-430deebefe8f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249495(v=office.15)
ms:contentKeyID: 48545756
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 21f1484850a91d1fbdbe687f171e8ae9dfe4a5cd
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936466"
---
# <a name="chapter-13-rds-usage-and-security"></a><span data-ttu-id="1cb53-102">Capítulo 13: Segurança e o uso do RDS</span><span class="sxs-lookup"><span data-stu-id="1cb53-102">Chapter 13: RDS usage and security</span></span>

<span data-ttu-id="1cb53-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1cb53-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1cb53-p101">Use as informações deste capítulo para configurar seu servidor e usar o RDS rapidamente. Este capítulo inclui etapas de configuração específicas das quais você pode precisar ao implementar o RDS, descreve algumas das relações-chave entre o RDS e outras tecnologias e ajuda a identificar as soluções para os problemas que podem ser encontrados ao configurar uma solução RDS.</span><span class="sxs-lookup"><span data-stu-id="1cb53-p101">Use the information in this chapter to set up your server and use RDS quickly. This chapter includes specific configuration steps that you might need to take when implementing RDS, describes some of the key relationships between RDS and other technologies, and helps identify solutions to problems that you might encounter when setting up an RDS solution.</span></span>

<span data-ttu-id="1cb53-106">Esta seção contém informações sobre:</span><span class="sxs-lookup"><span data-stu-id="1cb53-106">This section contains information about:</span></span>

- [<span data-ttu-id="1cb53-107">Configurando o DataFactory para modos safe ou unrestricted</span><span class="sxs-lookup"><span data-stu-id="1cb53-107">Configuring DataFactory for safe or unrestricted modes</span></span>](configuring-datafactory-for-safe-or-unrestricted-modes.md)
- [<span data-ttu-id="1cb53-108">Configurando o RDS</span><span class="sxs-lookup"><span data-stu-id="1cb53-108">Configuring RDS</span></span>](configuring-rds.md)
- [<span data-ttu-id="1cb53-109">Configurando servidores virtuais no IIS</span><span class="sxs-lookup"><span data-stu-id="1cb53-109">Configuring virtual servers on IIS</span></span>](configuring-virtual-servers-on-iis.md)
- [<span data-ttu-id="1cb53-110">Personalização de DataFactory (ADO)</span><span class="sxs-lookup"><span data-stu-id="1cb53-110">DataFactory customization (ADO)</span></span>](datafactory-customization.md)
- [<span data-ttu-id="1cb53-111">Permitindo que uma DLL seja executada no DCOM</span><span class="sxs-lookup"><span data-stu-id="1cb53-111">Enabling a DLL to run on DCOM</span></span>](enabling-a-dll-to-run-on-dcom.md)
- <span data-ttu-id="1cb53-112">[Concedendo privilégios de convidados a um computador do servidor web; Privilégios de convidados RDS \[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span><span class="sxs-lookup"><span data-stu-id="1cb53-112">[Granting guest privileges to a web server computer; RDS guest privileges \[ADO\]](granting-guest-privileges-to-a-web-server-computer;-rds-guest-privileges.md)</span></span>
- [<span data-ttu-id="1cb53-113">Marcando os objetos de negócios como seguros para script</span><span class="sxs-lookup"><span data-stu-id="1cb53-113">Marking business objects as safe for scripting</span></span>](marking-business-objects-as-safe-for-scripting.md)
- [<span data-ttu-id="1cb53-114">Registrar objetos de negócios no cliente para usam com o DCOM</span><span class="sxs-lookup"><span data-stu-id="1cb53-114">Registering business objects on the client for use with DCOM</span></span>](registering-business-objects-on-the-client-for-use-with-dcom.md)
- [<span data-ttu-id="1cb53-115">Protegendo aplicativos RDS</span><span class="sxs-lookup"><span data-stu-id="1cb53-115">Securing RDS applications</span></span>](securing-rds-applications.md)
- [<span data-ttu-id="1cb53-116">Configurando o DCOM stream marshaling format</span><span class="sxs-lookup"><span data-stu-id="1cb53-116">Setting DCOM stream marshaling format</span></span>](setting-dcom-stream-marshaling-format.md)
- [<span data-ttu-id="1cb53-117">Especificando encadeamentos por processador no IIS</span><span class="sxs-lookup"><span data-stu-id="1cb53-117">Specifying threads per processor on IIS</span></span>](specifying-threads-per-processor-on-iis.md)
- [<span data-ttu-id="1cb53-118">Solucionando problemas do RDS (ADO)</span><span class="sxs-lookup"><span data-stu-id="1cb53-118">Troubleshooting RDS (ADO)</span></span>](troubleshooting-rds.md)
- [<span data-ttu-id="1cb53-119">Usando tecnologias relacionadas com o RDS (ADO)</span><span class="sxs-lookup"><span data-stu-id="1cb53-119">Using related technologies with RDS (ADO)</span></span>](using-related-technologies-with-rds.md)















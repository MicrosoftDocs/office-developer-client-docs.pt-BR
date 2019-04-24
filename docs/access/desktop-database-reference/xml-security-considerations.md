---
title: Considerações sobre segurança no XML
TOCTitle: XML Security Considerations
ms:assetid: ef2c7f59-f5a2-98d1-37c6-42cb35b26a40
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250214(v=office.15)
ms:contentKeyID: 48548575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 648e7980be19f8af39cdb5e19858ba1ffd16518e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308243"
---
# <a name="xml-security-considerations"></a><span data-ttu-id="0e49e-102">Considerações sobre segurança XML</span><span class="sxs-lookup"><span data-stu-id="0e49e-102">XML security considerations</span></span>


<span data-ttu-id="0e49e-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e49e-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="xml-security-considerations"></a><span data-ttu-id="0e49e-104">Considerações sobre segurança no XML</span><span class="sxs-lookup"><span data-stu-id="0e49e-104">XML Security Considerations</span></span>

<span data-ttu-id="0e49e-p101">Os métodos **Save** e **Open** do ADO no objeto **Recordset** não são considerados operações seguras para serem executadas no Internet Explorer. Assim, se esses métodos forem usados em um código de script que está sendo executado em um aplicativo ou controle hospedado em um navegador, a configuração de segurança do navegador terá um efeito sobre o seu comportamento.</span><span class="sxs-lookup"><span data-stu-id="0e49e-p101">The ADO **Save** and **Open** methods on the **Recordset** object are not considered safe operations to run in Internet Explorer. Thus, if these methods are used in a script code that is running in an application or control that is hosted in a browser, the security configuration of the browser will have an effect on its behavior.</span></span>

<span data-ttu-id="0e49e-p102">O Internet Explorer 5 oferece restrições de segurança para tais operações por padrão nas zonas de Internet. Sob essa configuração, o **Recordset** não pode fazer nenhum acesso ao sistema de arquivos local no cliente nem acessar quaisquer fontes de dados fora do domínio do servidor a partir do qual a página será baixada. Especificamente, ao executar no host do navegador, um **Recordset** pode ser salvo novamente em um arquivo apenas se ele estiver no mesmo servidor a partir do qual a página foi baixada. De maneira semelhante, você pode abrir um **Recordset** carregando-o a partir de um arquivo apenas se esse arquivo estiver no mesmo servidor a partir do qual a página foi baixada.</span><span class="sxs-lookup"><span data-stu-id="0e49e-p102">Internet Explorer 5 provides security restrictions for such operations by default in the Internet zones. Under that configuration, the **Recordset** cannot make any access to the local file system on the client or access any data sources outside the domain of the server from which the page has been downloaded. Specifically, when running inside the browser host, a **Recordset** can be saved back to a file only if it is on the same server from which the page was downloaded. Similarly, you can open a **Recordset** by loading it from a file only if that file is on the same server from which the page was downloaded.</span></span>

<span data-ttu-id="0e49e-111">Para obter mais informações sobre segurança no Internet Explorer, consulte o artigo técnico "Problemas de segurança no ADO e RDS no Microsoft Internet Explorer."</span><span class="sxs-lookup"><span data-stu-id="0e49e-111">For more information about security in Internet Explorer, see the technical article "ADO and RDS Security Issues in Microsoft Internet Explorer."</span></span>


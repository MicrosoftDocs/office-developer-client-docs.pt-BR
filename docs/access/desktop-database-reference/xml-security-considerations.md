---
title: Considerações sobre segurança no XML
TOCTitle: XML Security Considerations
ms:assetid: ef2c7f59-f5a2-98d1-37c6-42cb35b26a40
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250214(v=office.15)
ms:contentKeyID: 48548575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 69672b2993cb91ace5bd447b762f33fcbd66c1bc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868487"
---
# <a name="xml-security-considerations"></a>Considerações sobre segurança no XML


**Aplica-se a**: Access 2013, o Office 2013

## <a name="xml-security-considerations"></a>Considerações sobre segurança XML

Os métodos **Save** e **Open** do ADO no objeto **Recordset** não são considerados operações seguras para serem executadas no Internet Explorer. Assim, se esses métodos forem usados em um código de script que está sendo executado em um aplicativo ou controle hospedado em um navegador, a configuração de segurança do navegador terá um efeito sobre o seu comportamento.

O Internet Explorer 5 oferece restrições de segurança para tais operações por padrão nas zonas de Internet. Sob essa configuração, o **Recordset** não pode fazer nenhum acesso ao sistema de arquivos local no cliente nem acessar quaisquer fontes de dados fora do domínio do servidor a partir do qual a página será baixada. Especificamente, ao executar no host do navegador, um **Recordset** pode ser salvo novamente em um arquivo apenas se ele estiver no mesmo servidor a partir do qual a página foi baixada. De maneira semelhante, você pode abrir um **Recordset** carregando-o a partir de um arquivo apenas se esse arquivo estiver no mesmo servidor a partir do qual a página foi baixada.

Para obter mais informações sobre segurança no Internet Explorer, consulte o artigo técnico "Problemas de segurança no ADO e RDS no Microsoft Internet Explorer."


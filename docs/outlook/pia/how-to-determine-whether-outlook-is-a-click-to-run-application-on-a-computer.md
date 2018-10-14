---
title: Determinar se o Outlook é um aplicativo Clique para Executar em um computador
TOCTitle: Determine whether Outlook is a Click-to-Run application on a computer
ms:assetid: 1b8573be-8ea8-4973-869d-87fda57ce525
ms:mtpsurl: https://msdn.microsoft.com/library/Ff522355(v=office.15)
ms:contentKeyID: 55119804
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: c155fed72a314c5c260ed2fe574474afd45c44c3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406649"
---
# <a name="determine-whether-outlook-is-a-click-to-run-application-on-a-computer"></a>Determinar se o Outlook é um aplicativo Clique para Executar em um computador

Clique para Executar é um mecanismo de distribuição e atualização de software disponível para o Office 2010 e versões posteriores. Produtos fornecidos por meio de Clique para Executar em um ambiente virtual de aplicativo no sistema operacional local. Isso significa que eles têm particulares cópias de seus arquivos e configurações, e as alterações que fazem são capturadas no ambiente virtual.

O Clique para Executar é rápido: os usuários podem começar a executar um aplicativo em pouco tempo, sem ter que esperar que o produto completo conclua a instalação. As atualizações são executadas automaticamente em segundo plano, sem precisar que um usuário primeiro remova uma instalação ou instale as atualizações manualmente. Produtos Clique para Executar são virtualizados e não entram em conflito com outro software instalado. No entanto, como um produto Clique para Executar tem cópias particulares de todos os respectivos arquivos e registros, um desenvolvedor de suplemento não consegue determinar a existência do produto da mesma forma que um produto instalado no disco rígido do computador do cliente. Desde o Outlook 2010, os desenvolvedores de suplementos devem verificar se o Outlook está instalado e se o Outlook foi entregue como um produto Clique para Executar.


> [!NOTE]
> Somente o Office 2013 de 32 bits tem suporte para o ambiente virtual de aplicativos Clique para Executar, mesmo se o computador cliente usar um sistema operacional de 64 bits.



### <a name="to-check-whether-outlook-2013-was-delivered-by-click-to-run-on-a-client-computer"></a>Para verificar se o Outlook 2013 foi entregue pelo Clique para Executar em um computador cliente

- Verifique se a chave VirtualOutlook existe no seguinte local no registro do Windows:
    
  `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
    
  A chave VirtualOutlook é um valor REG\_SZ que contém a marca de cultura do idioma de produto instalado, como "pt-br".

## <a name="see-also"></a>Confira também

- [Suplemento de administração](add-in-administration.md)


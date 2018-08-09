---
title: Testar a implantação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: Este tópico descreve alguns cenários que você deve ser testado em relação a instalação e desinstalação de um provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 0494d2ecab446b7da091f80df02267e281987d8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770968"
---
# <a name="testing-deployment"></a>Testar a implantação

Este tópico descreve alguns cenários que você deve ser testado em relação a instalação e desinstalação de um provedor do Outlook Social Connector (OSC).

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Presença do Outlook e o OSC no computador cliente

Fatores o mesmo efeito que instalando um provedor OSC inclui o número de bits do sistema operacional, as informações de presença e bitness do Outlook e o OSC que está sendo habilitado no Outlook.
  
Um provedor OSC pode ser escrito para uma versão 32 bits ou 64 bits do OSC. Outlook 2010 e o Outlook 2013 estão disponíveis nas versões de 32 bits e 64 bits, e o Office Outlook 2003 e o Office Outlook 2007 estão disponíveis nas versões de 32 bits somente. Em um sistema operacional de Windows de 64 bits, você pode instalar o Outlook de 32 bits ou 64 bits. Em um sistema operacional de 32 bits, você pode instalar apenas 32 bits, mas não 64 bits, Outlook. Dependendo o número de bits da versão instalada do Outlook e o próprio provedor do OSC, o usuário deve usar o instalador apropriado para instalar um provedor OSC do número de bits apropriado. Por exemplo, se o Outlook de 64 bits é instalado e o provedor OSC é um componente nativo do COM, um provedor OSC de 32 bits não funcionarão e o usuário deve usar o instalador apropriado para instalar um provedor OSC de 64 bits.
  
O código de implantação do seu provedor OSC pode assumir que o usuário tem uma versão compatível do Outlook no computador. No entanto, se a versão atual do OSC não estiver no computador cliente, seu código de implantação pode baixar e instalar uma versão apropriada do OSC usando URLs especialmente construído g-link em http://g.live.com. Esses links de g dependem a versão e o número de bits do Outlook e a localidade do computador cliente. Para obter mais informações sobre como usar o g-links para instalar ou atualizar o OSC, consulte a [lista de verificação de instalação](installation-checklist.md).
  
Antes de instalar um provedor OSC, o usuário do Outlook deve assegurar que o suplemento do OSC está habilitado no Outlook.
  
O método recomendado de implantação de um provedor OSC é usar um pacote do Windows Installer (. msi). Teste cada um dos seguintes cenários para verificar a implantação funciona corretamente para o provedor.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|O Outlook não estiver presente - Outlook 2003 ou o Outlook 2007 não estiver instalado, Outlook 2010 ou o Microsoft Outlook 2013 não está instalado nem ele foi fornecido pela Click-to-Run.  <br/> |A implantação falhará.  <br/> |
|Outlook 2003 ou o Outlook 2007 não estiver instalado, mas o Outlook 2010 ou o Microsoft Outlook 2013 foi fornecido pela Click-to-Run.  <br/> |O provedor de 32 bits é implantado.  <br/> |
|Outlook 2003 ou o Outlook 2007 está instalado, mas o OSC não está instalado.  <br/> |O instalador é instalado o OSC e todos os patches. Depois que o OSC tiver sido instalado com êxito, o instalador implanta o provedor.  <br/> |
|Outlook 2003 ou o Outlook 2007 está instalado e se uma versão anterior do OSC está instalada.  <br/> |O instalador atualiza o OSC, por meio de um link de g patches e, em seguida, implanta o provedor.  <br/> |
|Outlook 2003 ou 2007 está instalado e o OSC está atualizado.  <br/> |O instalador implanta o provedor de 32 bits.  <br/> |
|Outlook 2010 ou o Microsoft Outlook 2013 está instalado, mas o OSC não está instalado.  <br/> |O instalador falha com uma mensagem de erro apropriada.  <br/> |
|Outlook 2010 ou o Microsoft Outlook 2013 está instalado e uma versão mais antiga do que o OSC está instalada.  <br/> |O instalador que é apropriado para o número de bits do Outlook 2010 instalado ou Microsoft Outlook 2013, atualiza o OSC por meio do link de g para patches e, em seguida, implanta o provedor apropriado.  <br/> |
|Outlook 2010 ou o Microsoft Outlook 2013 é instalado e o OSC está atualizado.  <br/> |O instalador apropriado para o número de bits do Microsoft Outlook 2013 (32 bits ou 64 bits) ou do Outlook 2010 instalado implanta o provedor apropriado.  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>Instalados local e chaves do registro

Verifique o local do arquivo onde o seu provedor OSC tiver sido implantado e os locais no registro do Windows, onde as chaves do registro para seu provedor são criadas.
  
### <a name="file-location-for-osc-provider-dlls"></a>Local de arquivo para o provedor OSC DLLs

Teste para os cenários, conforme listado na tabela a seguir. Observe que a tabela lista os caminhos de instalação padrão para DLLs de provedor do OSC. Os usuários podem personalizar onde instalar essas DLLs.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|Microsoft Outlook 2013 está instalado no computador cliente.  <br/> |Provedor DLLs são implantados na pasta Office15. Se o sistema operacional é de 64 bits e o Microsoft Outlook 2013 é de 32 bits, as DLLs de 32 bits são implantadas em arquivos C:\Program (x86) \Microsoft Office\Office15. Se o sistema operacional é de 64 bits e o Microsoft Outlook 2013 é de 64 bits, as DLLs de 64 bits são implantadas em C:\Program Files\Microsoft Office\Office15. Se o sistema operacional é de 32 bits, DLLs são implantados em C:\Program Files\Microsoft Office\Office15.  <br/> |
|Outlook 2010 está instalado no computador cliente.  <br/> |Provedor DLLs são implantados para a pasta do Office14. Se o sistema operacional é de 64 bits e o Outlook 2010 é de 32 bits, as DLLs de 32 bits são implantadas em arquivos C:\Program (x86) \Microsoft Office\Office14. Se o sistema operacional é de 64 bits e o Outlook 2010 é de 64 bits, as DLLs de 64 bits são implantadas em C:\Program Files\Microsoft Office\Office14. Se o sistema operacional é de 32 bits, DLLs são implantados em C:\Program Files\Microsoft Office\Office14.  <br/> |
|Outlook 2007 está instalado no computador cliente.  <br/> |Provedor DLLs são implantados em C:\Program Files\Microsoft Office\Office14. Instalar o OSC cria a pasta Office14 e o OSC deve ser instalado antes de qualquer provedor DLLs. Consulte a seção anterior [presença do Outlook e o OSC no computador cliente](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Outlook 2003 é instalado no computador cliente.  <br/> |Provedor DLLs são implantados em C:\Program Files\Microsoft Office\Office14. Instalar o OSC cria a pasta Office14 e o OSC deve ser instalado antes de qualquer provedor DLLs. Consulte a seção anterior [presença do Outlook e o OSC no computador cliente](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Microsoft Outlook 2013 não está instalado, mas viabilizadas pela Click-to-Run no computador cliente.  <br/> |Provedor DLLs são implantados na pasta Office15. Se o sistema operacional é de 64 bits, 32 bits DLLs são implantados em arquivos C:\Program (x86) \Microsoft Office\Office15 ou C:\Program Files\Microsoft Office\Office15. Se o sistema operacional é de 32 bits, DLLs são implantados em C:\Program Files\Microsoft Office\Office15. Se a pasta Office15 não existir, a instalação cria a pasta.  <br/> |
|Outlook 2010 não está instalado, mas viabilizadas pela Click-to-Run no computador cliente.  <br/> |Provedor DLLs são implantados para a pasta do Office14. Se o sistema operacional é de 64 bits, 32 bits DLLs são implantados em arquivos C:\Program (x86) \Microsoft Office\Office14 ou C:\Program Files\Microsoft Office\Office14. Se o sistema operacional é de 32 bits, DLLs são implantados em C:\Program Files\Microsoft Office\Office14. Se a pasta Office14 não existir, a instalação cria a pasta.  <br/> |
   
### <a name="windows-registry-locations"></a>Locais de registro do Windows

Verifique o seguinte:
  
- O instalador do provedor OSC criará um valor ProgID para o provedor do OSC no registro do Windows, em um `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` ou `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`. 
    
- A exceção é se o computador cliente tiver o Outlook de 32 bits em execução em um sistema de operacional do Windows de 64 bits. Nesse caso, o ProgID é criado em um `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` ou `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.
    
- As chaves do registro devem ser o mesmo e no mesmo local se, em vez disso, as DLLs registradas por regsvr32.exe.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>Removendo a instalação

Estes são alguns testes para verificar se o processo de desinstalação funciona corretamente para seu provedor de OSC.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|Usuário escolhe desinstalar o provedor.  <br/> |O provedor desinstala os DLLs e limpa o registro.  <br/> |
|Usuário escolhe para cancelar o processo de desinstalação do provedor.  <br/> |O provedor cancela o processo de desinstalação e traz o usuário volta para o estado antes do processo de desinstalação de Introdução.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Registrando um provedor](registering-a-provider.md)  
- [Lista de verificação de instalação](installation-checklist.md)
- [Preparando-se para o lançamento de um provedor OSC](getting-ready-to-release-an-osc-provider.md)


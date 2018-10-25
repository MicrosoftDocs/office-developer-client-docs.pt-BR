---
title: Testar a implantação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: Este tópico descreve alguns cenários que você deve testar em relação à instalação e à desinstalação de um provedor do Conector Social do Outlook (OSC).
ms.openlocfilehash: 9c811683097a08b9f6e575d4ea2fee29cdd545d6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383930"
---
# <a name="testing-deployment"></a>Testar a implantação

Este tópico descreve alguns cenários que você deve testar em relação à instalação e à desinstalação de um provedor do Conector Social do Outlook (OSC).

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Presença do Outlook e do OSC no computador cliente

Os fatores que afetam a instalação de um provedor do OSC incluem o número de bits do sistema operacional, a presença e o número de bits do Outlook e a habilitação do OSC no Outlook.
  
Um provedor do OSC pode ser escrito para uma versão de 32 bits ou de 64 bits do OSC. O Outlook 2010 e 2013 estão disponíveis em versões de 32 bits e de 64 bits; o Office Outlook 2003 e 2007 estão disponíveis somente em versões de 32 bits. Em um sistema operacional Windows de 64 bits, você pode instalar o Outlook de 32 bits ou de 64 bits. Em um sistema operacional Windows de 32 bits, você só pode instalar o Outlook de 32 bits, não é possível instalar a versão de 64 bits. Dependendo do número de bits da versão instalada do Outlook e do provedor de OSC, o usuário deve usar o instalador apropriado para instalar um provedor do OSC com o número de bits apropriado. Por exemplo, se o Outlook de 64 bits estiver instalado e o provedor do OSC é um componente COM nativo, um provedor do OSC de 32 bits não funcionará e o usuário deverá usar o instalador apropriado para instalar um provedor do OSC de 64 bits.
  
O código de implantação do provedor do OSC pode assumir que o usuário tem uma versão compatível do Outlook no computador. No entanto, se a versão atual do OSC não estiver no computador cliente, o código de implantação pode baixar e instalar a versão apropriada do OSC usando URLs especialmente construídas do g-link em https://g.live.com. Esses g-links dependem da versão, do número de bits do Outlook e da localidade do computador cliente. Saiba mais sobre como usar g-links para instalar ou atualizar o OSC na [Lista de verificação da instalação](installation-checklist.md).
  
Antes de instalar um provedor do OSC, o usuário do Outlook deve garantir que o suplemento do OSC esteja habilitado no Outlook.
  
O método recomendado de implantação de um provedor do OSC é usar um pacote do Windows Installer (.msi). Teste cada um dos seguintes cenários para verificar se a implantação funciona adequadamente para o provedor.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|O Outlook não está presente: o Outlook 2003 ou 2007 não está instalado, o Outlook 2010 ou o Microsoft Outlook 2013 não está instalado e não foi entregue pelo Clique para Executar.  <br/> |A implantação falha.  <br/> |
|O Outlook 2003 ou 2007 não está instalado, mas o Outlook 2010 ou Microsoft Outlook 2013 foi entregue pelo Clique para Executar.  <br/> |O provedor de 32 bits é implantado.  <br/> |
|O Outlook 2003 ou 2007 está instalado, mas o OSC não está instalado.  <br/> |O instalador instala o OSC e todos os patches. Depois que o OSC for instalado com êxito, o instalador implantará o provedor.  <br/> |
|O Outlook 2003 ou 2007 está instalado e uma versão anterior do OSC está instalada.  <br/> |O instalador atualiza o OSC por meio do g-link com patches e depois implanta o provedor.  <br/> |
|O Outlook 2003 ou 2007 está instalado e o OSC está atualizado.  <br/> |O instalador implanta o provedor de 32 bits.  <br/> |
|O Outlook 2010 ou o Microsoft Outlook 2013 está instalado, mas o OSC não está instalado.  <br/> |O instalador falha com uma mensagem de erro apropriada.  <br/> |
|O Outlook 2010 ou o Microsoft Outlook 2013 está instalado e uma versão anterior do OSC está instalada.  <br/> |O instalador, que é apropriado para o número de bits do Outlook 2010 ou o Microsoft Outlook 2013 instalado, atualiza o OSC por meio do g-link com os patches e, em seguida, implanta o provedor apropriado.  <br/> |
|O Outlook 2010 ou o Microsoft Outlook 2013 está instalado e o OSC está atualizado.  <br/> |O instalador, que é apropriado para o número de bits do Outlook 2010 ou do Microsoft Outlook 2013 (32 bits ou 64 bits), implanta o provedor apropriado.  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>Local e chaves de registro instaladas

Verifique o local do arquivo em que o provedor do OSC foi implantado e os locais no registro do Windows em que as chaves do registro do provedor são criadas.
  
### <a name="file-location-for-osc-provider-dlls"></a>Local do arquivo para DLLs do provedor do OSC

Teste para os cenários, conforme listados na tabela a seguir. Observe que a tabela lista os caminhos de instalação padrão para DLLs do provedor do OSC. Os usuários podem personalizar onde instalar essas DLLs.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|O Microsoft Outlook 2013 está instalado no computador cliente.  <br/> |As DLLs do provedor são implantadas na pasta Office15. Se o sistema operacional for de 64 bits e o Microsoft Outlook 2013 for de 32 bits, as DLLs de 32 bits são implantadas em C:\Arquivos de Programas (x86)\Microsoft Office\Office15. Se o sistema operacional for de 64 bits e o Microsoft Outlook 2013 for de 64 bits, as DLLs de 64 bits são implantadas em C:\Arquivos de Programas\Microsoft Office\Office15. Se o sistema operacional for de 32 bits, as DLLs são implantadas em C:\Arquivos de Programas\Microsoft Office\Office15.  <br/> |
|O Microsoft Outlook 2010 está instalado no computador cliente.  <br/> |As DLLs do provedor são implantadas na pasta Office14. Se o sistema operacional for de 64 bits e o Microsoft Outlook 2010 for de 32 bits, as DLLs de 32 bits são implantadas em C:\Arquivos de Programas (x86)\Microsoft Office\Office14. Se o sistema operacional for de 64 bits e o Microsoft Outlook 2010 for de 64 bits, as DLLs de 64 bits são implantadas em C:\Arquivos de Programas\Microsoft Office\Office14. Se o sistema operacional for de 32 bits, as DLLs são implantadas em C:\Arquivos de Programas\Microsoft Office\Office14.  <br/> |
|O Outlook 2007 está instalado no computador cliente.  <br/> |As DLLs do provedor são implantadas em C:\Arquivos de Programas\Microsoft Office\Office14. Instalar o OSC cria a pasta Office14 e o OSC deve ser instalado antes de qualquer DLL do provedor. Consulte a sessão anterior [Presença do Outlook e do OSC no computador cliente](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|O Outlook 2003 está instalado no computador cliente.  <br/> |As DLLs do provedor são implantadas em C:\Arquivos de Programas\Microsoft Office\Office14. Instalar o OSC cria a pasta Office14 e o OSC deve ser instalado antes de qualquer DLL do provedor. Consulte a sessão anterior [Presença do Outlook e do OSC no computador cliente](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|O Microsoft Outlook 2013 não está instalado, mas foi entregue pelo Clique para Executar no computador cliente.  <br/> |As DLLs do provedor são implantadas na pasta Office15. Se o sistema operacional for de 64 bits, as DLLs de 32 bits são implantadas em C:\Arquivos de Programas (x86)\Microsoft Office\Office15 ou C:\Arquivos de Programas\Microsoft Office\Office15. Se o sistema operacional for de 32 bits, as DLLs são implantadas em C:\Arquivos de Programas\Microsoft Office\Office15. Se não existir, a instalação cria a pasta Office15.  <br/> |
|O Microsoft Outlook 2010 não está instalado, mas foi entregue pelo Clique para Executar no computador cliente.  <br/> |As DLLs do provedor são implantadas na pasta Office14. Se o sistema operacional for de 64 bits, as DLLs de 32 bits são implantadas em C:\Arquivos de Programas (x86)\Microsoft Office\Office14 ou C:\Arquivos de Programas\Microsoft Office\Office14. Se o sistema operacional for de 32 bits, as DLLs são implantadas em C:\Arquivos de Programas\Microsoft Office\Office14. Se não existir, a instalação cria a pasta Office14.  <br/> |
   
### <a name="windows-registry-locations"></a>Locais de registro do Windows

Verifique os itens a seguir:
  
- O instalador do provedor do OSC cria um valor ProgID para o provedor do OSC no registro do Windows em `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` ou em `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`. 
    
- Ocorre uma exceção se o computador cliente executar o Outlook de 32 bits em um sistema operacional Windows de 64 bits. Nesse caso, o ProgID é criado em `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` ou em `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.
    
- As chaves de registro devem ser as mesmas e no mesmo local se, ao invés disso, as DLLs forem registradas pelo regsvr32.exe.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>Remover a instalação

Estes são alguns testes para verificar se o processo de desinstalação funciona corretamente para o seu provedor do OSC.
  
|**Cenário**|**Comportamento esperado**|
|:-----|:-----|
|O usuário decide desinstalar o provedor.  <br/> |O provedor desinstala as DLLs e limpa o registro.  <br/> |
|O usuário escolhe cancelar o processo de desinstalação do provedor.  <br/> |O provedor cancela o processo de desinstalação e retorna o usuário para o estado anterior ao começo do processo de desinstalação.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Registrar um provedor](registering-a-provider.md)  
- [Lista de verificação da instalação](installation-checklist.md)
- [Preparar um provedor de OSC para lançamento](getting-ready-to-release-an-osc-provider.md)


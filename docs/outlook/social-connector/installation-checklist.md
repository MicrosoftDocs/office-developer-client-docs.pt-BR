---
title: Lista de verificação da instalação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: Este tópico descreve os pré-requisitos para instalar com êxito um provedor do Outlook Social Connector (OSC) e a instalação verifica se o instalador do seu provedor deve ser concluídas para funcionar corretamente.
ms.openlocfilehash: 8fec8523e57ad2678d02a0c5cbc1ad57340e5267
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395088"
---
# <a name="installation-checklist"></a>Lista de verificação da instalação

Este tópico descreve os pré-requisitos para instalar com êxito um provedor do Outlook Social Connector (OSC) e a instalação verifica se o instalador do seu provedor deve ser concluídas para funcionar corretamente.
  
## <a name="installation-overview"></a>Visão geral da instalação

Os usuários devem instalar provedores OSC somente se houver uma versão de suporte do Outlook e o OSC está instalado e habilitado no computador cliente. Suporte de versões do Outlook são o Office Outlook 2003, o Office Outlook 2007, o Outlook 2010 e o Outlook 2013 (instalado no computador cliente ou, no caso do Outlook 2010 e o Outlook 2013, viabilizadas pela Click-to-Run no computador cliente). Para garantir uma instalação bem-sucedida, o instalador do seu provedor deve fazer o seguinte:
  
- Verifique se uma versão compatível do Outlook está presente.
    
- Verificar se o OSC está instalado.
    
> [!NOTE]
> Click-to-Run é um ambiente virtual no qual o Outlook 2010 (32 bits) ou Outlook 2013 (32-bit) podem executar. Para o Outlook 2013, verifique se a chave VirtualOutlook existe no HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook do registro do Windows. Para obter mais informações sobre como entregar Outlook como um produto clique para executar em um computador cliente, consulte [como verificar se o Outlook está disponível em um computador como um produto Click-to-Run](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx). 
  
O usuário, no entanto, tem que garantir que o OSC está ativado antes de instalar o provedor.
  
Terceiros, incluindo provedores OSC, não é possível redistribuir o OSC. No entanto, se o OSC não estiver instalado, o instalador do provedor pode usar g-links apropriados para instalar o OSC no computador cliente. Um link de g é uma URL especialmente construída em https://g.live.com que encaminha um usuário para uma página da Web correspondente para baixar o OSC. Um link de g OSC é formatado como https://g.live.com/0CR _LCID_/ _Glink_, onde _LCID_ e _Glink_ especificam a localidade, versão e bitness do Outlook no computador cliente. Cada link de g aponta para um arquivo executável e é específico para os valores _LCID_ e _Glink_ especificados. 
  
Por exemplo, o g-link para instalar a versão mais recente do OSC para o Outlook 2003 ou o Outlook 2007 para o LCID 1033 (inglês americano) é da seguinte maneira:
  
https://g.live.com/0CR1033/80
  
Para obter detalhes sobre os valores de _Glink_ para diferentes versões e bitness do Outlook e valores _LCID_ para localidades com suporte, consulte #7 na seção [Lista de verificação de instalação](#olosc_InstallationOverview_InstallationChecklist) abaixo. 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>Lista de verificação da instalação

O pacote de instalação do provedor deve realizar uma série de verificações de instalação, conforme mostrado na Figura 1, para garantir que o provedor é instalado com êxito.
  
**Figura 1. Lógica de instalação do provedor**

![Lista de verificação da instalação](media/odc_ol14_ta_OSC_Fig07.gif)
  
O procedimento a seguir descreve as verificações de instalação descritas na Figura 1.
  
1. Como um pré-requisito, detectar se o Outlook está instalado ou apresentar e, se instalado ou presente, determine se a versão do Outlook suporta o OSC. Para obter mais informações sobre como detectar a versão instalada do Outlook, consulte [Verificar a versão do Outlook](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx).
    
   - Se a versão do Outlook instalada é anterior ao Outlook 2003, o procedimento de instalação do provedor não pode concluir. Informe o usuário para obter uma versão compatível do Outlook e o OSC antes de prosseguir para instalar o provedor OSC.
    
   - Se o Outlook não estiver instalado, vá para a etapa 2.
    
   - Se o Outlook 2003 ou o Outlook 2007 está instalado, vá para a etapa 3. 
    
   - Se o Outlook 2010 ou Outlook 2013 está instalado, vá para a etapa 4.
    
2. **Continue com esta etapa se o Outlook não está instalado no computador cliente:**
    
   1. Verifique se o OSC está instalado como um componente de padrão de uma instalação Click-to-Run do Outlook 2010 ou Outlook 2013. Examinar o `VirtualOutlook` chave no seguinte local no registro do Windows: 
      
      - Para o Outlook 2010,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - Para o conector Social do Outlook 2013,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      O `VirtualOutlook` chave é um valor REG_SZ que contenha a marca de localidade, como "en-us", do produto instalado. 
      
   2. Se o `VirtualOutlook` chave não existir, o Outlook não estiver presente no computador cliente e o procedimento de instalação do provedor não pode ser concluída. Informe o usuário para obter uma versão compatível do Outlook e o OSC antes de prosseguir para instalar o provedor OSC. 
      
   3. Se o `VirtualOutlook` chave existir, o Outlook foi entregue por Click-to-Run no computador cliente. Vá para verificar a versão instalada do biblioteca de tipos do OSC examinando o `OSCVersion` chave no seguinte local no registro do Windows: 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      O valor da `OSCVersion` é uma cadeia de caracteres que especifica o número de versão de biblioteca de tipo de Socialprovider.dll (por exemplo, "1.0", "1.1" ou "15"). 
      
   4. Se `OSCVersion` é "1.0", "1.1" ou "15", uma versão apropriada do OSC está instalada. Vá para a etapa 6 para encontrar a localidade da interface de usuário do Outlook atual para se preparar para instalação da versão mais recente do OSC. 
      
   5. Caso contrário, `OSCVersion` não contiver um valor esperado. Vá para a etapa 6 para encontrar a localidade da interface de usuário do Outlook atual para se preparar para instalar uma versão apropriada do OSC. 
    
3. **Continue com esta etapa se o Outlook 2003 ou o Outlook 2007 estiver instalado no computador cliente:**
    
   1. Verificar se o OSC é instalado por escrever um instalador ação personalizada para testar a existência da seguinte ID de componente qualificado:
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      A ID do componente qualificado é um GUID que fornece um método de único nível indireção, semelhante a um ponteiro. Para obter mais informações sobre o Windows Installer, consulte o [roteiro para a documentação do Windows Installer](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation).
      
   2. Se o componente qualificado especificado existir, uma versão do OSC é instalada. Vá para a etapa 5 para encontrar a localidade da interface de usuário do Outlook atual para se preparar para instalação da versão mais recente do OSC.
      
   3. Caso contrário, o OSC não está instalado. Vá para a etapa 6 para encontrar a localidade da interface de usuário do Outlook atual para se preparar para instalar uma versão apropriada do OSC.
      
4. **Continue com esta etapa se o Outlook 2010 ou Outlook 2013 estiver instalado no computador cliente:**
    
   1. Determinar o número de bits da versão instalada do Outlook examinando o `Bitness` chave no seguinte local no registro do Windows: 
      
      - Para o Outlook 2010, examinar`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - Para o Outlook 2013, examinar`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      O `Bitness` chave é "x86" para o Outlook de 32 bits ou "x64" para o Outlook de 64 bits. 
      
   2. Se seu provedor for um provedor gerenciado e compilado do componente de provedor, especificando a plataforma de destino como **Any CPU**, continue a etapa 6 para encontrar a localidade da interface de usuário do Outlook atual para se preparar para instalação da versão mais recente do OSC. Seu provedor funcionará em versões de 32 bits e 64 bits do OSC.
      
   3. Se seu provedor for um componente nativo do COM, examine o número de bits da versão instalada do Outlook:
      
      - Se a versão instalada do Outlook é de 32 bits, o procedimento de instalação será preciso instalar um provedor de 32 bits (na etapa 8), depois que você assegurar que uma OSC adequado está instalado.
      
      - Caso contrário, a versão instalada do Outlook é de 64 bits, e o procedimento de instalação será preciso instalar um provedor de 64 bits (na etapa 8), depois que você assegurar que uma OSC adequado está instalado. 
      
   4. Continue com a etapa 6 para encontrar a localidade da interface de usuário do Outlook atual para se preparar para instalar uma versão apropriada do OSC.
    
5. **Continuar com esta etapa se o Outlook 2003 ou o Outlook 2007 está instalado e se o OSC está instalado no computador cliente:** Verifique a localidade de interface de usuário atual do Outlook, examinando o `OSCLcid` chave no seguinte local no registro do Windows: 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   O `OSCLcid` chave é um valor DWORD que especifica a marca de localidade de Internet Engineering Task Force (IETF) (definida pelas [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) e [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)), que representa a localidade de interface de usuário atual do Outlook. Continue a etapa 7 para instalar o OSC mais recente no computador cliente.
    
6. **Continue com esta etapa se o Outlook 2003 ou o Outlook 2007 está instalado, ou o Outlook 2010 ou Outlook 2013 está presente, mas o mais recente OSC necessariamente não estiver instalado no computador cliente:**
    
   Use o objeto **LanguageSettings** para determinar o LCID da localidade de interface de usuário do Outlook. O trecho de código Visual Basic Scripting Edition (VBScript) a seguir demonstra como obter o LCID da localidade de interface de usuário do Outlook. 
    
   ```vb
    Function GetOutlookUI_LCID()
        ' Declare variables.
        Dim msoLanguageIDUI, olApp
        msoLanguageIDUI = 2
        Set olApp = CreateObject("Outlook.Application")
        ' Return Outlook UI LCID.
        GetOutlookUI_LCID = olApp.LanguageSettings.LanguageID(msoLanguageIDUI)
    End Function
   ```

7. **Continue com esta etapa se o instalador não tem o LCID da versão instalada do Outlook, mas o mais recente OSC necessariamente não estiver instalado no computador cliente:**
    
   Encadear um link de g em seu pacote de instalação para assegurar que a versão mais recente do que o OSC seja instalada no computador cliente. O formato de vínculo g é da seguinte maneira:
    
   https://g.live.com/0CR_LCID_ /  _Glink_
    
   Consulte a tabela 1 a seguir para valores _LCID_ suportados e a tabela 2 para os valores de _Glink_ com suporte. Por exemplo, o link de g para instalar a versão mais recente do OSC de 32 bits para 32 bits Outlook Social Connector 2013 (inglês americano) é da seguinte maneira: 
    
   https://g.live.com/0CR1033/82
    
8. Instale o fornecedor. O procedimento de instalação do provedor deve registrar o identificador programático (ProgID) no local apropriado de registro do Windows. Para obter mais informações, consulte [Registrando um provedor](registering-a-provider.md). Além disso, certifique-se de que o número de bits do provedor a ser instalada é o mesmo que o número de bits da versão do Outlook presente no computador cliente. Por exemplo, instale um provedor de 32 bits, se houver Outlook 2013 de 32 bits e um provedor de 64 bits, se o Outlook 2013 de 64 bits é instalado. Para o Outlook 2003 ou 2007, se aplica somente a versão de 32 bits do seu provedor. 
    
**Tabela 1: Localidade com suporte e valores LCID correspondentes em hexadecimal para que o OSC**
  
|**Localidade**|**LCID**|
|:-----|:-----|
|ar-sa  <br/> |1025  <br/> |
|bg-bg  <br/> |1026  <br/> |
|CA-es  <br/> |1027  <br/> |
|cs-cz  <br/> |1029  <br/> |
|da-dk  <br/> |1030  <br/> |
|de-de  <br/> |1031  <br/> |
|el-gr  <br/> |1032  <br/> |
|en-us  <br/> |1033  <br/> |
|es-es  <br/> |3082  <br/> |
|et-ee  <br/> |1061  <br/> |
|es da UE  <br/> |1069  <br/> |
|fi-fi  <br/> |1035  <br/> |
|fr-fr  <br/> |1036  <br/> |
|GL-es  <br/> |1110  <br/> |
|he-il  <br/> |1037  <br/> |
|hi-in  <br/> |1081  <br/> |
|hr-hr  <br/> |1050  <br/> |
|hu-hu  <br/> |1038  <br/> |
|it-it  <br/> |1040  <br/> |
|ja-jp  <br/> |1041  <br/> |
|kk-kz  <br/> |1087  <br/> |
|ko-kr  <br/> |1042  <br/> |
|lt-lt  <br/> |1063  <br/> |
|lv-lv  <br/> |1062  <br/> |
|nb-no  <br/> |1044  <br/> |
|nl-nl  <br/> |1043  <br/> |
|pl-pl  <br/> |1045  <br/> |
|pt-br  <br/> |1046  <br/> |
|pt-pt  <br/> |2070  <br/> |
|ro-ro  <br/> |1048  <br/> |
|ru-ru  <br/> |1049  <br/> |
|sk-sk  <br/> |1051  <br/> |
|sl-si  <br/> |1060  <br/> |
|SR-cyrl-cs  <br/> |3098  <br/> |
|SR-latn-cs  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |
   
**Tabela 2: Valores de Glink com suporte para que o OSC**
  
|**Valor GLINK**|**Função**|
|:-----|:-----|
|80  <br/> |Instala a versão mais recente do OSC para o Outlook 2003 ou o Outlook 2007.  <br/> |
|82  <br/> |Instala o patch mais recente do OSC de 32 bits para o Outlook 2007, Outlook 2010 ou Outlook Social Connector 2013.  <br/> |
|83  <br/> |Instala o patch mais recente do OSC de 64 bits para o Outlook 2010 ou Outlook Social Connector 2013.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Registrando um provedor](registering-a-provider.md) 
- [Etapas rápidas de aprendizado para desenvolver um provedor](quick-steps-for-learning-to-develop-a-provider.md)
- [Implantando um provedor](deploying-a-provider.md)


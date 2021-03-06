---
title: Lista de verificação da instalação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: Este tópico descreve os pré-requisitos para instalar com êxito um provedor do Outlook Social Connector (OSC) e verifica se o instalador do provedor deve ser concluído para funcionar corretamente.
ms.openlocfilehash: 8fec8523e57ad2678d02a0c5cbc1ad57340e5267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286334"
---
# <a name="installation-checklist"></a>Lista de verificação da instalação

Este tópico descreve os pré-requisitos para instalar com êxito um provedor do Outlook Social Connector (OSC) e verifica se o instalador do provedor deve ser concluído para funcionar corretamente.
  
## <a name="installation-overview"></a>Visão geral da instalação

Os usuários devem instalar provedores OSC somente se uma versão de suporte do Outlook estiver presente e o OSC estiver instalado e habilitado no computador cliente. As versões de suporte do Outlook são o Office Outlook 2003, o Office Outlook 2007, o Outlook 2010 e o Outlook 2013 (instalados no computador cliente ou, no caso do Outlook 2010 e do Outlook 2013, fornecidos pelo Clique para Executar no computador cliente). Para garantir uma instalação bem-sucedida, o instalador do provedor deve fazer o seguinte:
  
- Verifique se uma versão com suporte do Outlook está presente.
    
- Verifique se o OSC está instalado.
    
> [!NOTE]
> Clique para Executar é um ambiente virtual no qual o Outlook 2010 (32 bits) ou o Outlook 2013 (32 bits) podem ser executados. For Outlook 2013, verify if the VirtualOutlook key exists in HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook of the Windows registry. For more information about delivering Outlook as a Click-to-Run product on a client computer, see [How to Verify if Outlook is Available on a Computer as a Click-to-Run Product](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx). 
  
O usuário, no entanto, precisa garantir que o OSC está habilitado antes de instalar o provedor.
  
Terceiros, incluindo provedores OSC, não podem redistribuir o OSC. No entanto, se o OSC não estiver instalado, o instalador do provedor poderá usar links g apropriados para instalar o OSC no computador cliente. Um g-link é uma URL especialmente construída que encaminha um usuário para uma página da Web correspondente https://g.live.com para baixar o OSC. Um g-link do OSC é formatado como https://g.live.com/0CR _Glink LCID,_ onde /   _LCID_ e _Glink_ especificam a localidade, a versão e o bitness do Outlook no computador cliente. Cada g-link aponta para um executável e é específico para os valores _LCID_ e _Glink especificados._ 
  
Por exemplo, o g-link para instalar a versão mais recente do OSC para Outlook 2003 ou Outlook 2007 para lCID 1033 (inglês dos EUA) é o seguinte:
  
https://g.live.com/0CR1033/80
  
Para obter detalhes sobre os valores do  _Glink_ para diferentes versões e o bitness do Outlook e valores  _LCID_ para localidades com suporte, consulte #7 na seção Lista de verificação de [instalação](#olosc_InstallationOverview_InstallationChecklist) abaixo. 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>Lista de verificação da instalação

O pacote de instalação do provedor deve executar uma série de verificações de instalação, conforme mostrado na Figura 1, para garantir que o provedor seja instalado com êxito.
  
**Figura 1. Lógica de instalação do provedor**

![Lista de verificação da instalação](media/odc_ol14_ta_OSC_Fig07.gif)
  
O procedimento a seguir descreve as verificações de instalação descritas na Figura 1.
  
1. Como pré-requisito, detecte se o Outlook está instalado ou presente e, se instalado ou presente, determine se a versão do Outlook é compatível com o OSC. For more information about detecting the installed version of Outlook, [see Check the Version of Outlook](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx).
    
   - Se a versão instalada do Outlook for anterior ao Outlook 2003, o procedimento de instalação do provedor não poderá ser concluído. Informe o usuário para obter uma versão com suporte do Outlook e do OSC antes de prosseguir para instalar o provedor do OSC.
    
   - Se o Outlook não estiver instalado, prossiga para a etapa 2.
    
   - Se o Outlook 2003 ou o Outlook 2007 estiver instalado, prossiga para a etapa 3. 
    
   - Se o Outlook 2010 ou o Outlook 2013 estiver instalado, prossiga para a etapa 4.
    
2. **Prossiga com esta etapa se o Outlook não estiver instalado no computador cliente:**
    
   1. Verifique se o OSC está instalado como um componente padrão de uma instalação Clique para Executar do Outlook 2010 ou do Outlook 2013. Examine a  `VirtualOutlook` chave no seguinte local no Registro do Windows: 
      
      - Para o Outlook 2010,  `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - Para o Outlook Social Connector 2013,  `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      A chave é um REG_SZ que contém a marca de localidade, como  `VirtualOutlook` "en-us", do produto instalado. 
      
   2. Se a chave não existir, o Outlook não estará presente no computador cliente e o procedimento de instalação do provedor  `VirtualOutlook` não poderá ser concluído. Informe o usuário para obter uma versão com suporte do Outlook e do OSC antes de prosseguir para instalar o provedor do OSC. 
      
   3. Se a  `VirtualOutlook` chave existir, o Outlook foi entregue pelo Clique para Executar no computador cliente. Prossiga para verificar a versão instalada da biblioteca de tipos do OSC examinando a chave no seguinte local no  `OSCVersion` Registro do Windows: 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      O valor é uma cadeia de caracteres que especifica o número de versão da biblioteca de tipos  `OSCVersion` de Socialprovider.dll (por exemplo, "1.0", "1.1" ou "15"). 
      
   4. Se  `OSCVersion` for "1.0", "1.1" ou "15", uma versão apropriada do OSC será instalada. Prossiga para a etapa 6 para encontrar a localidade atual da interface do usuário do Outlook para se preparar para instalar a versão mais recente do OSC. 
      
   5. Caso contrário,  `OSCVersion` não contém um valor esperado. Prossiga para a etapa 6 para encontrar a localidade atual da interface do usuário do Outlook para preparar a instalação de uma versão apropriada do OSC. 
    
3. **Prossiga com esta etapa se o Outlook 2003 ou o Outlook 2007 estiver instalado no computador cliente:**
    
   1. Verifique se o OSC está instalado escrevendo uma ação personalizada do instalador para testar a existência da seguinte ID de componente qualificado:
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      A ID do componente qualificado é um GUID que fornece um método de indcisão de nível único, semelhante a um ponteiro. Para obter mais informações sobre o Windows Installer, [consulte Roadmap para a documentação do Windows Installer.](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation)
      
   2. Se o componente qualificado especificado existir, uma versão do OSC será instalada. Prossiga para a etapa 5 para encontrar a localidade atual da interface do usuário do Outlook para se preparar para instalar a versão mais recente do OSC.
      
   3. Caso contrário, o OSC não será instalado. Prossiga para a etapa 6 para encontrar a localidade atual da interface do usuário do Outlook para preparar a instalação de uma versão apropriada do OSC.
      
4. **Prossiga com esta etapa se o Outlook 2010 ou o Outlook 2013 estiver instalado no computador cliente:**
    
   1. Determine o bitness da versão instalada do Outlook examinando a chave no  `Bitness` seguinte local no Registro do Windows: 
      
      - Para o Outlook 2010, confira  `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - For Outlook 2013, look at  `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      A  `Bitness` chave é "x86" para o Outlook de 32 bits ou "x64" para o Outlook de 64 bits. 
      
   2. Se o provedor for um provedor gerenciado e você compilou o componente do provedor especificando a plataforma de destino como **Cpu** Any, prossiga com a etapa 6 para encontrar a localidade atual da interface do usuário do Outlook para se preparar para instalar a versão mais recente do OSC. Seu provedor funcionará nas versões de 32 bits e 64 bits do OSC.
      
   3. Se o provedor for um componente COM nativo, examine o bitness da versão instalada do Outlook:
      
      - Se a versão instalada do Outlook for de 32 bits, o procedimento de instalação terá que instalar um provedor de 32 bits (na etapa 8), depois de garantir que um OSC apropriado está instalado.
      
      - Caso contrário, a versão instalada do Outlook será de 64 bits e o procedimento de instalação terá que instalar um provedor de 64 bits (na etapa 8), depois de garantir que um OSC apropriado seja instalado. 
      
   4. Prossiga com a etapa 6 para encontrar a localidade atual da interface do usuário do Outlook para preparar a instalação de uma versão apropriada do OSC.
    
5. Prossiga com esta etapa se o **Outlook 2003 ou o Outlook 2007** estiver instalado e o OSC estiver instalado no computador cliente: Verifique a localidade atual da interface do usuário do Outlook examinando a `OSCLcid` chave no seguinte local no Registro do Windows: 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   A chave é um valor DWORD que especifica a marca de localidade da  `OSCLcid` Internet Engineering Task Force (IETF) (definida por [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) e [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)), que representa a localidade atual da interface do usuário do Outlook. Prossiga com a etapa 7 para instalar o OSC mais recente no computador cliente.
    
6. **Prossiga com esta etapa se o Outlook 2003 ou o Outlook 2007 estiver instalado ou se o Outlook 2010 ou o Outlook 2013 estiver presente, mas o OSC mais recente não estiver necessariamente instalado no computador cliente:**
    
   Use o **objeto LanguageSettings** para determinar o LCID da localidade da interface do usuário do Outlook. O seguinte trecho de código do Visual Basic Scripting Edition (VBScript) demonstra como obter o LCID da localidade da interface do usuário do Outlook. 
    
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

7. **Prossiga com esta etapa se o instalador tiver o LCID da versão instalada do Outlook, mas o OSC mais recente não estiver necessariamente instalado no computador cliente:**
    
   Encadeia um g-link ao pacote de instalação para garantir que a versão mais recente do OSC seja instalada no computador cliente. O formato g-link é o seguinte:
    
   https://g.live.com/0CR_LCID_ /  _Glink_
    
   Consulte a Tabela 1 abaixo para ver os valores  _LCID_ com suporte e a Tabela 2 para os valores  _de Glink com_ suporte. Por exemplo, o g-link para instalar a versão mais recente do OSC de 32 bits para o Outlook Social Connector 2013 de 32 bits (inglês dos EUA) é o seguinte: 
    
   https://g.live.com/0CR1033/82
    
8. Instale o provedor. O procedimento de instalação do provedor deve registrar o identificador programático (ProgID) no local apropriado do Registro do Windows. Para obter mais informações, [consulte Registro de um provedor.](registering-a-provider.md) Além disso, certifique-se de que o número de bits do provedor a ser instalado seja o mesmo que o número de bits da versão do Outlook presente no computador cliente. Por exemplo, instale um provedor de 32 bits se o Outlook 2013 de 32 bits estiver presente e um provedor de 64 bits se o Outlook 2013 de 64 bits estiver instalado. Para o Outlook 2003 ou 2007, somente a versão de 32 bits do seu provedor se aplica. 
    
**Tabela 1: Localidade suportada e valores LCID correspondentes em hexadecimal para o OSC**
  
|**Locale**|**LCID**|
|:-----|:-----|
|ar-sa  <br/> |1025  <br/> |
|bg-bg  <br/> |1026  <br/> |
|ca-es  <br/> |1027  <br/> |
|cs-cz  <br/> |1029  <br/> |
|da-dk  <br/> |1030  <br/> |
|de-de  <br/> |1031  <br/> |
|el-gr  <br/> |1032  <br/> |
|en-us  <br/> |1033  <br/> |
|es-es  <br/> |3082  <br/> |
|et-ee  <br/> |1061  <br/> |
|eu-es  <br/> |1069  <br/> |
|fi-fi  <br/> |1035  <br/> |
|fr-fr  <br/> |1036  <br/> |
|gl-es  <br/> |1110  <br/> |
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
|sr-cyrl-cs  <br/> |3098  <br/> |
|sr-latn-cs  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |
   
**Tabela 2: Valores de Glink com suporte para o OSC**
  
|**Valor do Glink**|**Function**|
|:-----|:-----|
|80  <br/> |Instala a versão mais recente do OSC para Outlook 2003 ou Outlook 2007.  <br/> |
|82  <br/> |Instala o patch mais recente do OSC de 32 bits para Outlook 2007, Outlook 2010 ou Outlook Social Connector 2013.  <br/> |
|83  <br/> |Instala o patch mais recente do OSC de 64 bits para o Outlook 2010 ou o Outlook Social Connector 2013.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Registrar um provedor](registering-a-provider.md) 
- [Etapas rápidas para aprender a desenvolver um provedor](quick-steps-for-learning-to-develop-a-provider.md)
- [Implantar um provedor](deploying-a-provider.md)


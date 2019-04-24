---
title: Lista de verificação da instalação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9dfb9b6d-2fb4-45bf-a12f-bd10a799ce29
description: Este tópico descreve os pré-requisitos para instalar com êxito um provedor do Outlook Social Connector (OSC) e a instalação verifica se o seu instalador de provedor deve ser concluído para funcionar corretamente.
ms.openlocfilehash: 8fec8523e57ad2678d02a0c5cbc1ad57340e5267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286334"
---
# <a name="installation-checklist"></a>Lista de verificação da instalação

Este tópico descreve os pré-requisitos para instalar com êxito um provedor do Outlook Social Connector (OSC) e a instalação verifica se o seu instalador de provedor deve ser concluído para funcionar corretamente.
  
## <a name="installation-overview"></a>Visão geral da instalação

Os usuários devem instalar provedores do OSC somente se uma versão de suporte do Outlook estiver presente e o OSC estiver instalado e habilitado no computador cliente. O suporte a versões do Outlook é o Office Outlook 2003, Office Outlook 2007, Outlook 2010 e Outlook 2013 (instalado no computador cliente ou, no caso do Outlook 2010 e do Outlook 2013, fornecido por clique para executar no computador cliente). Para garantir uma instalação bem-sucedida, o instalador do provedor deve fazer o seguinte:
  
- Verifique se há suporte para a versão do Outlook.
    
- Verifique se o OSC está instalado.
    
> [!NOTE]
> Clique para executar é um ambiente virtual no qual o Outlook 2010 (32 bits) ou o Outlook 2013 (32 bits) podem ser executados. Para o Outlook 2013, verifique se a chave VirtualOutlook existe no HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook do registro do Windows. Para obter mais informações sobre como entregar o Outlook como um produto clique para executar em um computador cliente, consulte [como verificar se o Outlook está disponível em um computador como um produto clique para executar](https://blogs.msdn.com/b/officedevdocs/archive/2010/03/09/how-to-verify-if-outlook-is-available-on-a-computer-as-a-click-to-run-product.aspx). 
  
No entanto, o usuário deve garantir que o OSC esteja habilitado antes da instalação do provedor.
  
Terceiros, incluindo provedores OSC, não podem redistribuir o OSC. No enTanto, se o OSC não estiver instalado, o instalador do provedor poderá usar os links g apropriados para instalar o OSC no computador cliente. Um g-link é uma URL criada especialmente no https://g.live.com que encaminha um usuário para uma página da Web correspondente para baixar o OSC. Um link g-link é formatado como https://g.live.com/0CR _LCID_/ _Glink_, onde _LCID_ e _Glink_ especificam a localidade, a versão e o meio de bits do Outlook no computador cliente. Cada g-link aponta para um executável e é específico para os valores _LCID_ e _Glink_ especificados. 
  
Por exemplo, o g-link para instalar a versão mais recente do OSC para Outlook 2003 ou o Outlook 2007 para o LCID 1033 (inglês dos EUA) é o seguinte:
  
https://g.live.com/0CR1033/80
  
Para obter detalhes sobre os valores de _Glink_ para diferentes versões e bits do Outlook e os valores _LCID_ para localidades compatíveis, consulte #7 na [lista de verificação de instalação](#olosc_InstallationOverview_InstallationChecklist) de seção abaixo. 

<a name="olosc_InstallationOverview_InstallationChecklist"> </a>

## <a name="installation-checklist"></a>Lista de verificação da instalação

O pacote de instalação do provedor deve executar uma série de verificações de instalação, conforme mostrado na Figura 1, para garantir que o provedor seja instalado com êxito.
  
**Figura 1. Lógica de instalação do provedor**

![Lista de verificação da instalação](media/odc_ol14_ta_OSC_Fig07.gif)
  
O procedimento a seguir descreve as verificações de instalação descritas na Figura 1.
  
1. Como pré-requisito, detectar se o Outlook está instalado ou presente e, se estiver instalado ou presente, determinar se a versão do Outlook oferece suporte ao OSC. Para obter mais informações sobre a detecção da versão instalada do Outlook, consulte [verificar a versão do Outlook](https://msdn.microsoft.com/library/672fc380-a29b-4e99-9211-949fd5065723%28Office.15%29.aspx).
    
   - Se a versão instalada do Outlook for anterior ao Outlook 2003, o procedimento de instalação do provedor não poderá ser concluído. Informe o usuário para obter uma versão com suporte do Outlook e do OSC antes de prosseguir com a instalação do provedor do OSC.
    
   - Se o Outlook não estiver instalado, vá para a etapa 2.
    
   - Se o Outlook 2003 ou o Outlook 2007 estiver instalado, prossiga para a etapa 3. 
    
   - Se o Outlook 2010 ou o Outlook 2013 estiver instalado, prossiga para a etapa 4.
    
2. **Prossiga com esta etapa se o Outlook não estiver instalado no computador cliente:**
    
   1. Verifique se o OSC está instalado como um componente padrão de uma instalação clique para executar do Outlook 2010 ou do Outlook 2013. Examine a `VirtualOutlook` chave no seguinte local no registro do Windows: 
      
      - Para o Outlook 2010,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\14.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      - Para o Outlook Social Connector 2013,`HKEY_LOCAL_MACHINE\Software\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
      
      A `VirtualOutlook` chave é um valor REG_SZ que contém a marca de localidade, como "en-US", do produto instalado. 
      
   2. Se a `VirtualOutlook` chave não existir, o Outlook não estará presente no computador cliente e o procedimento de instalação do provedor não poderá ser concluído. Informe o usuário para obter uma versão com suporte do Outlook e do OSC antes de prosseguir com a instalação do provedor do OSC. 
      
   3. Se a `VirtualOutlook` chave existir, o Outlook foi entregue pelo clique para executar no computador cliente. Continue para verificar a versão instalada da biblioteca de tipos OSC examinando a `OSCVersion` chave no seguinte local no registro do Windows: 
      
      `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCVersion`
      
      O valor de `OSCVersion` é uma cadeia de caracteres que especifica o número de versão da biblioteca de tipos do socialprovider. dll (por exemplo, "1,0", "1,1" ou "15"). 
      
   4. Se `OSCVersion` for "1,0", "1,1" ou "15", uma versão apropriada do OSC será instalada. Vá para a etapa 6 para localizar a localidade da interface do usuário atual do Outlook para se preparar para a instalação da versão mais recente do OSC. 
      
   5. Caso contrário `OSCVersion` , não conterá um valor esperado. Vá para a etapa 6 para localizar a localidade da interface do usuário atual do Outlook para se preparar para a instalação de uma versão apropriada do OSC. 
    
3. **Prossiga com esta etapa se o Outlook 2003 ou o Outlook 2007 estiver instalado no computador cliente:**
    
   1. Verifique se o OSC está instalado escrevendo uma ação personalizada do instalador para testar a existência da seguinte ID de componente qualificado:
      
      `{A3B82DA3-8AD9-4935-AEA8-54B754459483}`
      
      A ID do componente qualificado é um GUID que fornece um método de indireção de nível único, semelhante a um ponteiro. Para obter mais informações sobre o Windows Installer, consulte [Roadmap to Windows Installer Documentation](https://docs.microsoft.com/windows/desktop/msi/roadmap-to-windows-installer-documentation).
      
   2. Se o componente qualificado especificado existir, uma versão do OSC será instalada. Vá para a etapa 5 para localizar a localidade atual da interface do usuário do Outlook para se preparar para a instalação da versão mais recente do OSC.
      
   3. Caso contrário, o OSC não está instalado. Vá para a etapa 6 para localizar a localidade da interface do usuário atual do Outlook para se preparar para a instalação de uma versão apropriada do OSC.
      
4. **Prossiga com esta etapa se o Outlook 2010 ou o Outlook 2013 estiver instalado no computador cliente:**
    
   1. Determine a verificação de bits da versão instalada do Outlook examinando `Bitness` a chave no seguinte local no registro do Windows: 
      
      - Para o Outlook 2010, consulte`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\14.0\Outlook`
      
      - Para o Outlook 2013, consulte`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Outlook`
      
      A `Bitness` chave é "x86" para 32-bit Outlook ou "x64" para o outlook de 64 bits. 
      
   2. Se seu provedor é um provedor gerenciado e você compilou o componente do provedor que especifica a plataforma de destino como **qualquer CPU**, prossiga com a etapa 6 para localizar a localidade da interface do usuário atual do Outlook para se preparar para a instalação da versão mais recente do OSC. Seu provedor funcionará em ambas as versões de 32 bits e 64 bits do OSC.
      
   3. Se seu provedor for um componente COM nativo, examine o meio de bits da versão instalada do Outlook:
      
      - Se a versão instalada do Outlook for 32 bits, seu procedimento de instalação terá que instalar um provedor de 32 bits (na etapa 8), depois de verificar se um OSC apropriado está instalado.
      
      - Caso contrário, a versão instalada do Outlook será de 64 bits, e o procedimento de instalação terá que instalar um provedor de 64 bits (na etapa 8), depois de verificar se um OSC apropriado está instalado. 
      
   4. Prossiga com a etapa 6 para localizar a localidade da interface do usuário atual do Outlook para se preparar para a instalação de uma versão apropriada do OSC.
    
5. **Prossiga com esta etapa se o outlook 2003 ou o outlook 2007 estiver instalado e o OSC estiver instalado no computador cliente:** Verifique a localidade atual da interface do usuário do Outlook `OSCLcid` examinando a chave no seguinte local no registro do Windows: 
    
   `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\OSCLcid`
    
   A `OSCLcid` chave é um valor DWORD que especifica a marca de localidade da Internet Engineering Task Force (IETF) (definida por [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) e [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)), que representa a localidade de interface do usuário atual do Outlook. Prossiga com a etapa 7 para instalar o OSC mais recente no computador cliente.
    
6. **Prossiga com esta etapa se o Outlook 2003 ou o Outlook 2007 estiver instalado ou se o Outlook 2010 ou o Outlook 2013 estiver presente, mas o último OSC não estiver necessariamente instalado no computador cliente:**
    
   Use o objeto **LanguageSettings** para determinar o LCID da localidade da interface do usuário do Outlook. O seguinte trecho de código do Visual Basic Scripting Edition (VBScript) demonstra como obter o LCID da localidade de interface do usuário do Outlook. 
    
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
    
   Vincule um g-link ao seu pacote de instalação para garantir que a versão mais recente do OSC esteja instalada no computador cliente. O formato g-link é o seguinte:
    
   https://g.live.com/0CR_LCID_ /  _Glink_
    
   Consulte a tabela 1 abaixo para obter os valores _LCID_ suportados e tabela 2 para os valores de _Glink_ com suporte. Por exemplo, o g-link para instalar a última versão do 32-bit OSC para o Outlook Social Connector 2013 (inglês dos EUA) é o seguinte: 
    
   https://g.live.com/0CR1033/82
    
8. Instale o provedor. O procedimento de instalação do provedor deve registrar o identificador programático (ProgID) no local apropriado do registro do Windows. Para obter mais informações, consulte [registro de um provedor](registering-a-provider.md). Além disso, certifique-se de que a bits do provedor a ser instalado seja a mesma da versão do Outlook presente no computador cliente. Por exemplo, instale um provedor de 32 bits se o Outlook 2013 de 32 bits estiver presente e um provedor de 64 bits se o Outlook 64 de 2013 bits estiver instalado. Para o Outlook 2003 ou 2007, somente a versão de 32 bits do seu provedor se aplica. 
    
**Tabela 1: localidade com suporte e valores LCID correspondentes em hexadecimal para o OSC**
  
|**LCID**|**LCID**|
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
|Sr-Cyrl-CS  <br/> |3098  <br/> |
|Sr-LATN-CS  <br/> |2074  <br/> |
|sv-se  <br/> |1053  <br/> |
|th-th  <br/> |1054  <br/> |
|tr-tr  <br/> |1055  <br/> |
|uk-ua  <br/> |1058  <br/> |
|zh-cn  <br/> |2052  <br/> |
|zh-tw  <br/> |1028  <br/> |
   
**Tabela 2: valores de Glink com suporte para o OSC**
  
|**Valor Glink**|**Function**|
|:-----|:-----|
|80  <br/> |Instala a versão mais recente do OSC para Outlook 2003 ou o Outlook 2007.  <br/> |
|82  <br/> |Instala o patch mais recente do OSC de 32 bits para o Outlook 2007, Outlook 2010 ou Outlook Social Connector 2013.  <br/> |
|83  <br/> |Instala o patch mais recente do OSC 64-bit para o Outlook 2010 ou o Outlook Social Connector 2013.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Registrar um provedor](registering-a-provider.md) 
- [Etapas rápidas para aprender a desenvolver um provedor](quick-steps-for-learning-to-develop-a-provider.md)
- [Implantar um provedor](deploying-a-provider.md)


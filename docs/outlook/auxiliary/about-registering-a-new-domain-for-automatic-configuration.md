---
title: Sobre como registrar um novo domínio para configuração automática
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a7ab8a50-dd30-4ba5-b6d8-e6d1f482e6f1
description: O Outlook fornece uma maneira de especificar um novo domínio de serviço de mensagem para configuração automática e permite que o provedor de serviços de mensagem configure a conta.
ms.openlocfilehash: bf06ff8d145ed6173e3545f784f8b5b7b5f433be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316965"
---
# <a name="about-registering-a-new-domain-for-automatic-configuration"></a>Sobre como registrar um novo domínio para configuração automática

O Outlook fornece uma maneira de especificar um novo domínio de serviço de mensagem para configuração automática e permite que o provedor de serviços de mensagem configure a conta.
  
Durante a criação de um provedor de serviços de mensagem, você pode usar a seguinte chave do registro do Windows para especificar um novo domínio a ser configurado automaticamente pelo provedor de serviços de mensagem correspondente: 
  
`HKLM\Software\Microsoft\Office\Outlook\AutoConfigDomains\<domain name>\`
  
A chave, `<domain name>` é o domínio para a configuração automática. Um caractere curinga dá suporte a esse nome de domínio \* apenas no início. A tabela a seguir mostra os valores que tem suporte para essa tecla. 
  
| Valor | Tipo | Descrição |
|:-----|:-----|:-----|
|Nome Amigável  <br/> |REG_SZ  <br/> |O nome de domínio é exibido para o usuário durante a configuração automática.  <br/> |
|Nome do Serviço  <br/> |REG_SZ  <br/> |A mensagem de serviço registrada no Mapisvc que ofereça suporte a esse domínio.  <br/> |
|Local de instalação  <br/> |REG_SZ  <br/> |A URL do local para instalar o provedor de serviços de mensagem se ele ainda não estiver instalado.  <br/> |
|Versão mínima  <br/> |REG_DWORD  <br/> |A versão mínima. dll do provedor de serviços de mensagem é necessária. Esse valor é opcional.  <br/> |
   
Quando o Outlook começa a configuração automática de uma conta de email, ele verifica o registro do Windows para o registro de domínio especificado pelo endereço de email. Se o domínio já estiver especificado no registro do Windows, o Outlook verifica se o serviço está registrado no Mapisvc.inf. O Outlook não consegue prosseguir com a configuração automática do domínio, a não ser que ela tenha sido especificada no registro do Windows.
  
Se o serviço de mensagem especificado no momento não estiver registrado no Mapisvc.inf., ou se o provedor de serviços de mensagem estiver instalado, mas com uma versão do .dll anterior ao mínimo especificado, o Outlook usará o nome amigável especificado e solicitará ao usuário para que instale o provedor. Se o usuário aceitar, o Outlook irá redirecionar o usuário para o local de instalação especificado para que o usuário possa instalar o provedor. Instalar o provedor registra o serviço de mensagem no Mapisvc.
  
Se o serviço já estiver registrado no Mapisvc.inf e a versão do provedor de serviço. dll for apropriada, o Outlook criará o serviço[IMsgServiceAdmin::CreateMsgService](https://msdn.microsoft.com/library/0135f049-0311-45e5-9685-78597d599a4e%28Office.15%29.aspx)e irá confirmar usando [IMsgServiceAdmin::ConfigureMsgService](https://msdn.microsoft.com/library/a08f5905-2585-49ca-abb7-a77f2736f604%28Office.15%29.aspx). A configuração automática do Outlook usa as três seguintes propriedades para permitir que o provedor de configure a conta: [PidTagAutoConfigurationUserName](https://msdn.microsoft.com/library/05dfa0e2-4ab1-4f57-9009-6a815aca87bd%28Office.15%29.aspx), [PidTagAutoConfigurationUserEmail](https://msdn.microsoft.com/library/845140c8-5454-4b47-acec-ab5aff00b768%28Office.15%29.aspx)e [ PidTagAutoConfigurationUserPassword](https://msdn.microsoft.com/library/d33e7c45-55d8-4dc1-ade9-605542d87e61%28Office.15%29.aspx).
  
## <a name="see-also"></a>Confira também

- [Formato de arquivo de MapiSvc.inf](https://msdn.microsoft.com/library/b48eda17-83a8-4dc4-85c8-4ca827d13d25%28Office.15%29.aspx)


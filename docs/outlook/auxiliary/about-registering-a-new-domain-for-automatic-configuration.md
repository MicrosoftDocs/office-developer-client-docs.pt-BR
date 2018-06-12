---
title: Sobre como registrar um novo domínio para configuração automática
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a7ab8a50-dd30-4ba5-b6d8-e6d1f482e6f1
description: O Outlook oferece uma maneira para especificar um novo domínio de serviço de mensagem para a configuração automática e permitir que o provedor de serviços de mensagem configurar a conta.
ms.openlocfilehash: c1daea81fe18e5d1088a233a3fcdff076419d6bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765793"
---
# <a name="about-registering-a-new-domain-for-automatic-configuration"></a>Sobre como registrar um novo domínio para configuração automática

O Outlook oferece uma maneira para especificar um novo domínio de serviço de mensagem para a configuração automática e permitir que o provedor de serviços de mensagem configurar a conta.
  
Quando estiver criando um provedor de serviços de mensagem, você pode usar a seguinte chave no registro do Windows para especificar um novo domínio a ser configurado automaticamente pelo provedor de serviços de mensagem correspondente: 
  
`HKLM\Software\Microsoft\Office\Outlook\AutoConfigDomains\<domain name>\`
  
Na chave, `<domain name>` é o domínio para configuração automática. Este nome de domínio oferece suporte a um caractere curinga \* no início somente. A tabela a seguir mostra os valores que oferece suporte a essa chave. 
  
| Value | Tipo | Descrição |
|:-----|:-----|:-----|
|Nome amigável  <br/> |REG_SZ  <br/> |O nome de domínio que é exibido ao usuário durante a configuração automática.  <br/> |
|Nome do serviço  <br/> |REG_SZ  <br/> |O serviço de mensagem registrados no Mapisvc que ofereça suporte a esse domínio.  <br/> |
|Local de instalação  <br/> |REG_SZ  <br/> |A URL do local para instalar o provedor de serviços de mensagem, caso ele não ainda esteja instalado.  <br/> |
|Versão mínima  <br/> |REG_DWORD  <br/> |A versão mínima do arquivo. dll do provedor de serviços de mensagem que é necessário. Esse valor é opcional.  <br/> |
   
Quando o Outlook começa a configuração automática para uma conta de email, ele verifica o registro do Windows para o registro de domínio especificado pelo endereço de email. Se o domínio já está especificado no registro do Windows, o Outlook verifica se o serviço de mensagem está registrado no Mapisvc. O Outlook não poderá continuar com a configuração automática do domínio, a menos que tiver sido especificado no registro do Windows.
  
Se o serviço de mensagem especificado não está atualmente registrado no Mapisvc, ou o provedor de serviço de mensagem está instalado, mas o arquivo. dll tem uma versão anterior ao mínimo especificado, o Outlook usa o nome amigável especificado e solicita que o usuário instale o provedor. Se o usuário aceitar, o Outlook redireciona o usuário para o local de instalação especificado para que o usuário possa instalar o provedor. Instalar o provedor registra o serviço de mensagem no Mapisvc.
  
Se o serviço de mensagem está atualmente registrado no Mapisvc e o provedor de serviço. dll é uma versão apropriada, Outlook cria o serviço de mensagem usando [IMsgServiceAdmin:: CreateMsgService](http://msdn.microsoft.com/library/0135f049-0311-45e5-9685-78597d599a4e%28Office.15%29.aspx)e, em seguida, ele configura usando [ IMsgServiceAdmin::ConfigureMsgService](http://msdn.microsoft.com/library/a08f5905-2585-49ca-abb7-a77f2736f604%28Office.15%29.aspx). Configuração automática do Outlook utiliza as seguintes propriedades de três para permitir que o provedor configurar a conta: [PidTagAutoConfigurationUserName](http://msdn.microsoft.com/library/05dfa0e2-4ab1-4f57-9009-6a815aca87bd%28Office.15%29.aspx), [PidTagAutoConfigurationUserEmail](http://msdn.microsoft.com/library/845140c8-5454-4b47-acec-ab5aff00b768%28Office.15%29.aspx)e [PidTagAutoConfigurationUserPassword ](http://msdn.microsoft.com/library/d33e7c45-55d8-4dc1-ade9-605542d87e61%28Office.15%29.aspx).
  
## <a name="see-also"></a>Confira também

- [Formato de arquivo do Mapisvc](http://msdn.microsoft.com/library/b48eda17-83a8-4dc4-85c8-4ca827d13d25%28Office.15%29.aspx)


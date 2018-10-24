---
title: Registrar identificadores exclusivos do provedor de serviços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bde7ff73f58c8809d2dd6467daea28461e7c6ef7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586267"
---
# <a name="registering-service-provider-unique-identifiers"></a>Registrar identificadores exclusivos do provedor de serviços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Catálogo de endereços, armazenamento de mensagens e provedores de transporte usam um identificador exclusivo, conhecido como um [MAPIUID](mapiuid.md) para registrar para objetos de vários tipos de serviço. Um **MAPIUID** é um identificador de 16 bytes que contenha um GUID. Você pode criar um **MAPIUID** usando o procedimento a seguir: 
  
1. Defina uma constante.
    
2. Invocar o Visual Studio*Criar GUID** ferramenta. 
    
Por exemplo, um provedor de catálogo de endereços pode incluir a seguinte constante em um arquivo de cabeçalho para definir um **MAPIUID**:
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **Para registrar um MAPIUID se seu provedor for um provedor de repositório de catálogo ou mensagem de endereço**
  
1. Chame [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
    
2. Registrar um **MAPIUID** para cada logon do objeto que você instancia e incluir este **MAPIUID** nos primeiros 16 bytes do membro de cada identificador de entrada que você criar **ab** . MAPI usa estruturas **MAPIUID** para associar objetos de provedores de serviços. Quando a chamadas de cliente que o método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir um objeto, MAPI examina a parte **MAPIUID** do identificador de entrada, estabelecendo uma correspondência contra o registrados **MAPIUID**, para determinar qual objeto logon deve receber a abrir solicitação.
    
3. Se seu provedor for um transporte, registre uma ou mais estruturas **MAPIUID** quando seu método de **IXPLogon::AddressTypes** chamadas de MAPI. MAPI usa as estruturas **MAPIUID** registradas por provedores de transporte para atribuir a responsabilidade de entrega da mensagem. 
    
Embora os provedores de serviço geralmente registrar um único **MAPIUID**, você pode registrar várias estruturas de **MAPIUID** . Se seu catálogo de endereços ou mensagem armazenar provedor suporta vários objetos de logon, talvez, permitindo que um usuário para adicionar mais de uma instância do provedor de ao seu perfil, você talvez queira implementar um **MAPIUID** de diferentes para cada objeto de logon. Existem alguns outros motivos para dar suporte a mais de um **MAPIUID**:
  
- Você deve oferecer suporte a mais de uma versão do seu provedor e os identificadores de entrada devem representam a versão apropriada. Atribua um **MAPIUID** de diferentes para cada versão. 
    
- Você deseja distinguir entre os tipos de objetos que você ofereça suporte. Por exemplo, um provedor de catálogo de endereços talvez queira registrar um **MAPIUID** para usar os identificadores de entrada dos seus objetos de usuário de mensagens e um **MAPIUID** diferente a ser usado para listas de distribuição. 
    
Quando houver vários objetos de logon que estão ativos simultaneamente, faz sentido ter estruturas **MAPIUID** exclusivas para cada um deles. Isso aumenta a precisão com a qual o MAPI faz a correspondência de identificadores de entrada com provedores de serviços e salva algum trabalho. Quando cada objeto de logon tem seu próprio identificador exclusivo, MAPI pode garantir que qualquer solicitação rotas a um objeto de logon podem ser administradas por esse objeto. Quando os objetos de logon compartilham **MAPIUID** estruturas, MAPI encaminha a solicitação para o primeiro objeto de logon que é identificado pelo **MAPIUID**. Se um dos seus objetos logon recebe uma solicitação que não pode ser processada porque não processa o identificador de entrada, passa a solicitação de logon no seu próximo objeto logon antes de retornar um erro.
  
## <a name="see-also"></a>Confira também



[Implementação de Logon do provedor de serviço](implementing-service-provider-logon.md)


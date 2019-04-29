---
title: Registrando identificadores exclusivos do provedor de serviços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9f4acbb06f85a88a6c057da263ae95e09f72e0bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410172"
---
# <a name="registering-service-provider-unique-identifiers"></a>Registrando identificadores exclusivos do provedor de serviços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O catálogo de endereços, o repositório de mensagens e os provedores de transporte usam um identificador exclusivo conhecido como [MAPIUID](mapiuid.md) para registrar os objetos de serviço de vários tipos. Um **MAPIUID** é um identificador de 16 bytes que contém um GUID. Você pode criar um **MAPIUID** usando o procedimento a seguir: 
  
1. Definir uma constante.
    
2. Invocar a ferramenta*Create GUID** do Visual Studio. 
    
Por exemplo, um provedor de catálogo de endereços pode incluir a constante a seguir em um arquivo de cabeçalho para definir um **MAPIUID**:
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **Para registrar um MAPIUID se o seu provedor for um catálogo de endereços ou provedor de repositório de mensagens**
  
1. Chamar [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md).
    
2. Registre um **MAPIUID** para cada objeto de logon que você instancia e inclua esse **MAPIUID** nos primeiros 16 bytes do membro **AB** de cada identificador de entrada que você criar. MAPI usa estruturas **MAPIUID** para associar objetos com provedores de serviço. Quando um cliente chama o método [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir um objeto, o MAPI examina a parte **MAPIUID** do identificador de entrada, fazendo a correspondência com base no **MAPIUID**registrado, para determinar qual objeto de logon deve receber a abertura pedir.
    
3. Se seu provedor for um transporte, registre uma ou mais estruturas **MAPIUID** quando o MAPI chamar o método **IXPLogon:: AddressTypes** . MAPI usa as estruturas **MAPIUID** registradas por provedores de transporte para atribuir responsabilidade para entrega de mensagens. 
    
Embora os provedores de serviços normalmente registrem um único **MAPIUID**, você pode registrar várias estruturas do **MAPIUID** . Se o seu catálogo de endereços ou provedor de mensagens suportar vários objetos de logon, talvez por permitir que um usuário adicione mais de uma instância do seu provedor ao seu perfil, talvez você queira implementar um **MAPIUID** diferente para cada objeto de logon. Há alguns outros motivos para suportar mais de um **MAPIUID**:
  
- Você deve dar suporte a mais de uma versão de seu provedor e os identificadores de entrada devem representar a versão apropriada. Atribua um **MAPIUID** diferente para cada versão. 
    
- Você deseja distinguir entre os tipos de objetos com suporte. Por exemplo, um provedor de catálogo de endereços pode querer registrar um **MAPIUID** para usar nos identificadores de entrada de seus objetos de usuário de mensagens e um **MAPIUID** diferente para usar para listas de distribuição. 
    
Quando há vários objetos de logon simultaneamente ativos, faz sentido ter estruturas **MAPIUID** exclusivas para cada um. Isso aumenta a precisão com a qual o MAPI corresponde a identificadores de entrada para os provedores de serviço e salva algum trabalho. Quando cada objeto de logon tem seu próprio identificador exclusivo, o MAPI pode garantir que qualquer solicitação que ele roteia para um objeto de logon possa ser tratada por esse objeto. Quando os objetos de logon compartilham estruturas do **MAPIUID** , o MAPI encaminha a solicitação para o primeiro objeto de logon identificado pelo **MAPIUID**. Se um dos seus objetos de logon receber uma solicitação que ele não pode processar porque ele não lida com o identificador de entrada, passe a solicitação para o seu próximo objeto de logon antes de retornar um erro.
  
## <a name="see-also"></a>Confira também



[Implementar o logon do provedor de serviços](implementing-service-provider-logon.md)


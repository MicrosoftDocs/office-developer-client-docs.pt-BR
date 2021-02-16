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
  
Os provedores de transporte, armazenamento de mensagens e de agendamento de endereço usam um identificador exclusivo conhecido como [MAPIUID](mapiuid.md) para se registrar em objetos de serviço de vários tipos. Um **MAPIUID** é um identificador de 16 byte que contém um GUID. Você pode criar um **MAPIUID** usando o seguinte procedimento: 
  
1. Defina uma constante.
    
2. Invoque a ferramenta *Criar GUID** do Visual Studio. 
    
Por exemplo, um provedor de livros de endereços pode incluir a seguinte constante em um arquivo de título para definir um **MAPIUID**:
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 **Para registrar um MAPIUID se seu provedor for um provedor de armazenamento de mensagens ou de um livro de endereços**
  
1. Chame [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).
    
2. Registre **um MAPIUID** para cada objeto de logon que você criar e inclua esse **MAPIUID** nos primeiros 16 bytes do membro **ab** de cada identificador de entrada que você criar. O MAPI usa **estruturas MAPIUID** para associar objetos a provedores de serviços. Quando um cliente chama o método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir um objeto, o MAPI examina a parte **MAPIUID** do identificador de entrada, correspondendo-o ao **MAPIUID** registrado, para determinar qual objeto de logon deve receber a solicitação de abertura.
    
3. Se o provedor for um transporte, registre uma ou mais estruturas **MAPIUID** quando o MAPI chamar seu método **IXPLogon::AddressTypes.** MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery. 
    
Embora os provedores de serviços normalmente registrem um único **MAPIUID,** você pode registrar várias **estruturas MAPIUID.** Se o seu agendador de endereços ou o provedor de armazenamento de mensagens oferece suporte a vários objetos de logon, talvez permitindo que um usuário adicione mais de uma instância do seu provedor ao seu perfil, talvez você queira implementar um **MAPIUID** diferente para cada objeto de logon. Há alguns outros motivos para dar suporte a mais de um **MAPIUID:**
  
- Você deve dar suporte a mais de uma versão do seu provedor, e os identificadores de entrada devem representar a versão apropriada. Atribua um **MAPIUID diferente** para cada versão. 
    
- Você deseja distinguir entre os tipos de objetos com suporte. Por exemplo, um provedor de agendamento de endereços pode querer registrar um **MAPIUID** a ser usado nos identificadores de entrada de seus objetos de usuário de mensagens e um **MAPIUID** diferente para usar em listas de distribuição. 
    
Quando há vários objetos de logon atualmente ativos, faz sentido ter estruturas **MAPIUID** exclusivas para cada um deles. Isso aumenta a precisão com a qual o MAPI corresponde aos identificadores de entrada para provedores de serviços e economiza algum trabalho. Quando cada objeto de logon tem seu próprio identificador exclusivo, o MAPI pode garantir que qualquer solicitação encaminhada a um objeto de logon possa ser manipulada por esse objeto. Quando objetos de logon compartilham estruturas **MAPIUID,** MAPI encaminha a solicitação para o primeiro objeto de logon identificado pela **MAPIUID**. Se um dos objetos de logon receber uma solicitação que não pode processar porque não trata o identificador de entrada, passe a solicitação para o próximo objeto de logon antes de retornar um erro.
  
## <a name="see-also"></a>Confira também



[Implementando o logon do provedor de serviços](implementing-service-provider-logon.md)


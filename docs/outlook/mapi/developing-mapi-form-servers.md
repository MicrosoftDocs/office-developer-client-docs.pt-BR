---
title: Desenvolvendo servidores de formulário MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 63aa9db19c901f47004a7fe52d906846f44b8883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420763"
---
# <a name="developing-mapi-form-servers"></a>Desenvolvendo servidores de formulário MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Esta seção descreve o processo de criação de arquivos executáveis de servidor de formulários e de configuração de formulários para a criação de formulários MAPI personalizados. Antes de ler esta seção, você deve se familiarizar com as informações nos [formulários MAPI.](mapi-forms.md)
  
O desenvolvimento de um servidor de formulário inclui as seguintes etapas:
  
1. Decidir quais informações o formulário conterá e escolher um conjunto de propriedades para manter essas informações. For more information, see [Choosing a Form's Property Set](choosing-a-form-s-property-set.md).
    
2. Projetar uma interface do usuário com a qual os usuários podem interagir com as propriedades do formulário.
    
3. Escolher uma classe de mensagem e gerar um identificador de classe exclusivo (CLSID). Para uma visão geral das classes de mensagens, consulte [MAPI Message Classes](mapi-message-classes.md). Para obter mais informações sobre classes de mensagens e formulários, consulte [Escolhendo uma classe de mensagem.](choosing-a-message-class.md)
    
4. Implementando as interfaces de formulário MAPI necessárias, bem como quaisquer interfaces opcionais que seu servidor de formulário específico precisa. Para obter mais informações, consulte [Escrevendo código do servidor de formulário.](writing-form-server-code.md) 
    
5. Escrevendo o código da interface do usuário para manipular a interação do usuário com o objeto de formulário e as propriedades que o formulário usa.
    
6. Criando um arquivo de configuração de formulário para o formulário. Para obter mais informações, consulte [Formato de arquivo de arquivos de configuração de formulário.](file-format-of-form-configuration-files.md)
    
7. Instalando o formulário nos computadores dos usuários. Para obter mais informações, [consulte Instalando um formulário em uma biblioteca.](installing-a-form-into-a-library.md)
    
Você provavelmente executará as etapas de 1 a 5 simultaneamente, em vez de concluí-las em sequência. O processo de desenvolvimento de um servidor de formulário, como muitos projetos de programação, não é aquele em que há uma sequência particularmente bem definida. Por exemplo, a criação de um arquivo de configuração de formulário é mostrada como a segunda até a última etapa acima, mas você provavelmente criará seu arquivo de configuração de formulário incrementalmente e ele se tornará mais completo à medida que você adicionar recursos ao servidor de formulário.
  
## <a name="see-also"></a>Confira também



[Conceitos de MAPI](mapi-concepts.md)


---
title: Desenvolvimento de servidores de formulário MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30672a2d-2d39-4292-b21a-97a38485d1de
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 83d652f313e139b1c6bb628d1119edda03a70e23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766412"
---
# <a name="developing-mapi-form-servers"></a>Desenvolvimento de servidores de formulário MAPI

  
  
**Aplica-se a**: Outlook 
  
Esta seção descreve o processo de criação de servidor do formulário executável e arquivos de configuração de formulário para a criação de formulários personalizados de MAPI. Antes de ler esta seção, familiarize-se com as informações nos [Formulários de MAPI](mapi-forms.md).
  
Desenvolver um servidor de formulário inclui as seguintes etapas:
  
1. Decidindo quais informações que conterá o formulário e escolhendo um conjunto de propriedades para armazenar essas informações. Para obter mais informações, consulte [Escolher o conjunto de propriedade de um formulário](choosing-a-form-s-property-set.md).
    
2. Projetando uma interface de usuário com a qual os usuários podem interagir com as propriedades do formulário.
    
3. Escolhendo uma classe de mensagem e gerar um identificador exclusivo de classe (CLSID). Para obter uma visão geral das classes de mensagem, consulte [Classes de mensagem MAPI](mapi-message-classes.md). Para obter mais informações sobre formulários e classes de mensagens, consulte [escolhendo uma classe de mensagem](choosing-a-message-class.md).
    
4. Implementando as interfaces de formulário MAPI necessárias, bem como qualquer interfaces opcionais que precisa de seu servidor de formulário específico. Para obter mais informações, consulte [à escrita de código de servidor de formulário](writing-form-server-code.md). 
    
5. Como escrever o código de interface do usuário para manipular a interação do usuário com o objeto de formulário e as propriedades usa o formulário.
    
6. Criando um arquivo de configuração de formulário para o formulário. Para obter mais informações, consulte o [Arquivo de formato do formulário arquivos de configuração](file-format-of-form-configuration-files.md).
    
7. Instalando o formulário nos computadores dos usuários. Para obter mais informações, consulte [Instalando um formulário em uma biblioteca](installing-a-form-into-a-library.md).
    
Provavelmente você executará as etapas 1 a 5 simultaneamente em vez de concluí-las em uma sequência. O processo de desenvolvimento de um servidor de formulário, como muitos projetos de programação, não é um nos quais houver uma sequência particularmente bem definida. Por exemplo, criar um arquivo de configuração do formulário é mostrado como a segundo a última etapa acima, mas você provavelmente irá criar seu arquivo de configuração do formulário incrementalmente e tornarão mais completa conforme você adicionar recursos ao seu servidor do formulário.
  
## <a name="see-also"></a>Confira também



[Conceitos MAPI (em ingl�s)](mapi-concepts.md)


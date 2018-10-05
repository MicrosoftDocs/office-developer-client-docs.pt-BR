---
title: Cache de apelidos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: 'Modificado pela última vez: 30 de janeiro de 2013'
ms.openlocfilehash: 841b01ae8dfcf841b0a1d64113ce7258c4c61583
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389256"
---
# <a name="nickname-cache"></a>Cache de apelidos

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Microsoft Office Outlook 2007, Microsoft Outlook 2010 e Microsoft Outlook 2013 interagem com o cache de apelidos, também conhecido como "AutoCompletar stream." O fluxo de AutoCompletar é onde o Outlook mantém a lista de preenchimento automático, que é a lista de nomes que exibe o **para**, **Cc**e **Cco** caixas de edição enquanto um usuário está redigindo um email. Este tópico descreve como o Outlook 2007, Outlook 2010 e Outlook 2013 interagem com o fluxo de AutoCompletar e também aborda o formato binário do arquivo e as maneiras recomendadas para interagir com o fluxo de AutoCompletar. 
  
Para aplicativos que interagem com o Outlook 2010 ou Outlook 2013, o fluxo de AutoCompletar é armazenado como uma propriedade MAPI e pode ser modificado usando MAPI ou o objeto **PropertyAccessor** da mensagem. O objeto **PropertyAccessor** é exposto nos modelos de objeto do Outlook 2010 ou Outlook 2013. 
  
Não há nenhuma dependência no modelo de objeto do Outlook 2007 ou as APIs de MAPI. Portanto, os aplicativos que faça alterações para o fluxo de AutoCompletar dentro do Outlook 2007 podem ser escritos usando qualquer linguagem de programação.
  
## <a name="interacting-with-the-autocomplete-stream"></a>Interação com o fluxo de preenchimento automático

Quando as caixas de edição **para**, **Cc**ou **Cco** são acessadas em uma mensagem, o fluxo de AutoCompletar for carregado e a lista de nomes de usuário é exibida. Outlook interage com o fluxo de preenchimento automático de duas maneiras: 
  
1. Carregando o fluxo de preenchimento automático 
    
2. Salvar as alterações nos dados no stream autocomplete
    
Os meios de armazenar os dados de AutoCompletar difere entre o Outlook 2007 e Outlook 2010 ou Outlook 2013 da seguinte maneira: 
  
 **Outlook 2007**
  
Para o Outlook 2007, o fluxo de AutoCompletar é armazenado em um arquivo com o mesmo nome que o perfil e uma extensão de. nk2. Por exemplo, se o perfil padrão do "outlook" for usado, o arquivo será chamado "outlook.nk2". O arquivo. nk2 é armazenado na pasta % APPDATA%\Microsoft\Outlook. Para obter mais informações sobre o formato de arquivo binário do cache de apelidos, consulte o [formato de arquivo do Outlook 2003/2007 NK2 e diretrizes de desenvolvedor](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).
  
 **Outlook 2010 e o Outlook 2013**
  
Outlook 2010 ou Outlook 2013 lê o fluxo de preenchimento automático de uma mensagem na tabela associados conteúdo da caixa de entrada do repositório de entrega de uma conta de email. Essa mensagem oculta tem uma classe de mensagem e o assunto da IPM. Configuration.Autocomplete. O fluxo de AutoCompletar é armazenado nesta mensagem na propriedade PR_ROAMING_BINARYSTREAM ([PidTagRoamingBinary de propriedade canônico](pidtagroamingbinary-canonical-property.md)). Os dados de AutoCompletar podem ser temporariamente armazenados em cache em um arquivo. dat de AutoCompletar localizado em % USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache. No entanto, o arquivo. dat é apenas um cache e não é usado para gravar volta ao repositório de entrega, quando o usuário sai do Outlook 2010 ou Outlook 2013.
  
## <a name="loading-the-autocomplete-stream"></a>Carregando o fluxo de preenchimento automático

Outlook carrega o fluxo de AutoCompletar sempre que um item com a funcionalidade de endereçamento é inicializado. Por exemplo, endereços de email são usados em um novo email, uma resposta de email, um item de contato, uma solicitação de reunião e assim por diante. Para carregar os dados, o Outlook lê a todo o conteúdo do stream na memória.
  
Para operações de preenchimento automático, Outlook interage exclusivamente com esta estrutura na memória para toda a duração do tempo de vida de processo outlook.exe. Outlook salva apenas a estrutura em desligamento. Consulte a seção a seguir "Salvando o fluxo de AutoCompletar" para obter mais informações sobre esse processo.
  
## <a name="saving-the-autocomplete-stream"></a>Salvando o fluxo de preenchimento automático

Outlook salvar o fluxo de AutoCompletar durante o desligamento se a lista AutoCompletar foi alterado em qualquer uma das seguintes maneiras:
  
- Uma nova entrada de apelido for adicionada por meio de resolução de nomes, separação de um destinatário da caixa de diálogo Catálogo de endereços ou enviar um email para um destinatário que ainda não estava na lista.
    
- Uma entrada é modificada, enviando um email para um destinatário existente na lista.
    
- Uma entrada foi removida pelo usuário, através da interface do usuário.
    
- Outros cenários secundárias não relevantes para este tópico.
    
Salvar as alterações nos dados de AutoCompletar envolve a gravação da estrutura de na memória de volta para um [fluxo de AutoCompletar](autocomplete-stream.md). Ao interagir com o Outlook 2007, o fluxo é salvo em um arquivo. nk2 local. Para o Outlook 2010 ou Outlook 2013, o fluxo de AutoCompletar grava de volta para o índice de conteúdo associados de caixa de entrada do repositório de entrega de uma conta de email.
  
## <a name="recommendations"></a>Recomendações

- Nunca parcialmente modifica o fluxo de AutoCompletar. A interação com suporte é 1) ler o fluxo de AutoCompletar inteira na memória, 2) modificar a estrutura de memória e 3) gravar o fluxo inteiro volta tanto o índice de conteúdo associados de caixa de entrada do repositório de entrega de uma conta de email (para o Outlook 2010 ou Outlook 2013) ou para o arquivo. nk2 local (Outlook 2007).
    
- Não interagem com o fluxo de AutoCompletar durante a execução do Outlook. Se o Outlook estiver em execução enquanto você modifica o fluxo, ele provavelmente substituirá as alterações quando ele for desligado.
    
- Propriedades de gravação não de digite PT_MV_UNICODE e PR_MV_STRING8 em um fluxo de AutoCompletar a serem utilizados pelo Microsoft Outlook 2003. Essas propriedades só sejam entendidas pelo Outlook 2007, Outlook 2010 e Outlook 2013.
    
- Ao desenvolver o código que interage com o Outlook 2007, recomendamos que você bloquear o arquivo. nk2 contra modificação por outros processos enquanto você estiver lendo e gravando-lo usando o arquivo padrão de bloqueio de APIs (por exemplo, **LockFile** em C/C++ e ** FileStream.Lock** em c#). 
    
- Modifica apenas as propriedades de tipos que são provenientes do conjunto de linhas do fluxo de AutoCompletar. Para obter mais informações sobre as propriedades do fluxo de AutoCompletar e os tipos de propriedade, consulte [fluxo de AutoCompletar](autocomplete-stream.md).
    
## <a name="see-also"></a>Confira também



[Fluxo de preenchimento automático](autocomplete-stream.md)
  
[Perfis MAPI](mapi-profiles.md)


[Formato de arquivo do Outlook 2003/2007 NK2 e diretrizes de desenvolvedor](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)


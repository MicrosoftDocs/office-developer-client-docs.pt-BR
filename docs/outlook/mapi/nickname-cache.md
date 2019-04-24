---
title: Cache de apelidos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: 'Última modificação: 30 de janeiro de 2013'
ms.openlocfilehash: 841b01ae8dfcf841b0a1d64113ce7258c4c61583
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334514"
---
# <a name="nickname-cache"></a>Cache de apelidos

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O Microsoft Office Outlook 2007, o Microsoft Outlook 2010 e o Microsoft Outlook 2013 interagem com o cache de apelido, também conhecido como "fluxo de preenchimento automático". O fluxo de preenchimento automático é onde o Outlook persiste a lista de preenchimento automático, que é a lista de nomes exibidos nas caixas **de edição para**, **CC**e **Cco** enquanto um usuário está redigindo um email. Este tópico descreve como o Outlook 2007, o Outlook 2010 e o Outlook 2013 interagem com o fluxo de preenchimento automático e também discute o formato binário do arquivo e as maneiras recomendadas de interagir com o fluxo de preenchimento automático. 
  
Para aplicativos que interagem com o Outlook 2010 ou o Outlook 2013, o fluxo de preenchimento automático é armazenado como uma propriedade MAPI e pode ser modificado usando o objeto MAPI ou **PropertyAccessor** da mensagem. O objeto **PropertyAccessor** é exposto nos modelos de objeto do Outlook 2010 ou do Outlook 2013. 
  
Não há dependências no modelo de objeto do Outlook 2007 ou nas APIs MAPI. Portanto, os aplicativos que fazem alterações no fluxo de preenchimento automático no Outlook 2007 podem ser escritos usando qualquer linguagem de programação.
  
## <a name="interacting-with-the-autocomplete-stream"></a>Interagir com o fluxo de preenchimento automático

Quando as caixas de edição **para**, **CC**ou **Cco** são acessadas em uma mensagem, o fluxo de preenchimento automático é carregado e a lista de nomes de usuário é exibida. O Outlook interage com o fluxo de preenchimento automático de duas maneiras: 
  
1. Carregar o fluxo de preenchimento automático 
    
2. Salvando alterações nos dados no fluxo de preenchimento automático
    
O meio de armazenamento dos dados de preenchimento automático difere entre o Outlook 2007 e o Outlook 2010 ou o Outlook 2013 da seguinte maneira: 
  
 **Outlook 2007**
  
Para o Outlook 2007, o fluxo de preenchimento automático é armazenado em um arquivo com o mesmo nome do perfil e uma extensão de. nk2. Por exemplo, se o perfil padrão "Outlook" for usado, o arquivo será chamado de "Outlook. nk2". O arquivo. nk2 está armazenado no%APPDATA%\Microsoft\Outlook. Para obter mais informações sobre o formato de arquivo binário de cache de Alcunha, consulte [Outlook 2003/2007 NK2 File Format e developEr Guidelines](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).
  
 **Outlook 2010 e Outlook 2013**
  
O Outlook 2010 ou o Outlook 2013 lê o fluxo de preenchimento automático de uma mensagem na tabela de conteúdo associada da caixa de entrada do repositório de entrega da conta de email. Esta mensagem oculta tem uma classe de mensagem e o assunto de IPM. Configuration. AutoComplete. O fluxo de preenchimento automático é armazenado nessa mensagem na propriedade PR_ROAMING_BINARYSTREAM ([Propriedade canônica PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)). Os dados de preenchimento automático podem ser armazenados em cache temporariamente em um arquivo AutoComplete. dat localizado no%USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache. No enTanto, o arquivo. dat é apenas um cache e não é usado para gravar novamente no repositório de entrega quando o usuário sai do Outlook 2010 ou do Outlook 2013.
  
## <a name="loading-the-autocomplete-stream"></a>Carregar o fluxo de preenchimento automático

O Outlook carrega o fluxo de preenchimento automático sempre que um item com a funcionalidade de endereçamento é inicializado. Por exemplo, os endereços de email são usados em um novo email, uma resposta de email, um item de contato, uma solicitação de reunião e assim por diante. Para carregar os dados, o Outlook lê todo o conteúdo do fluxo na memória.
  
Para operações de preenchimento automático, o Outlook interage exclusivamente com essa estrutura na memória para a duração do tempo de vida do processo do Outlook. exe. O Outlook apenas salva a estrutura no desligamento. Consulte a seção a seguir "salvando o fluxo de preenchimento automático" para obter mais informações sobre esse processo.
  
## <a name="saving-the-autocomplete-stream"></a>Salvando o fluxo de preenchimento automático

O Outlook salvará o fluxo de preenchimento automático ao desligar se a lista de preenchimento automático tiver sido alterada de uma das seguintes maneiras:
  
- Uma nova entrada de apelido é adicionada através da resolução de um nome, da escolha de um destinatário da caixa de diálogo do catálogo de endereços ou de envio de email para um destinatário que ainda não estava na lista.
    
- Uma entrada é modificada enviando emails para um destinatário existente na lista.
    
- Uma entrada é removida pelo usuário por meio da interface do usuário.
    
- Outros cenários secundários não relevantes para este tópico.
    
Salvar alterações nos dados de preenchimento automático envolve gravar a estrutura na memória novamente em um [fluxo de preenchimento automático](autocomplete-stream.md). Ao interagir com o Outlook 2007, o Stream é salvo em um arquivo. nk2 local. Para o Outlook 2010 ou o Outlook 2013, o fluxo de preenchimento automático grava de volta para a tabela de conteúdo associada da caixa de entrada do repositório de entrega da conta de email.
  
## <a name="recommendations"></a>Recomendações

- Nunca modifique parcialmente o fluxo de preenchimento automático. A interação com suporte é de 1, ler todo o fluxo de AutoCompletar na memória, 2) modificar a estrutura da memória e 3) gravar todo o fluxo de volta para a tabela de conteúdo associada da caixa de entrada do repositório de entrega da conta de email (para o Outlook 2010 ou Outlook 2013) ou para o arquivo local. nk2 (Outlook 2007).
    
- Não interaja com o fluxo de preenchimento automático enquanto o Outlook estiver em execução. Se o Outlook estiver em execução enquanto você modifica o Stream, ele provavelmente substituirá as alterações quando ele fechar.
    
- Não grave Propriedades do tipo PT_MV_UNICODE e PR_MV_STRING8 em um fluxo de preenchimento automático para ser consumido pelo Microsoft Outlook 2003. Essas propriedades são compreendidas apenas pelo Outlook 2007, pelo Outlook 2010 e pelo Outlook 2013.
    
- Ao desenvolver um código que interaja com o Outlook 2007, recomendamos que você bloqueie o arquivo. nk2 de modificação por outros processos enquanto lê e grava-o usando APIs de bloqueio de arquivos padrão (por **** exemplo, lockfile no C/C++ e ** FileStream. Lock** em C#). 
    
- Só modifique as propriedades dos tipos que são do conjunto de linhas do fluxo de preenchimento automático. Para obter mais informações sobre as propriedades do fluxo de preenchimento automático e tipos de propriedade, consulte [AutoComplete Stream](autocomplete-stream.md).
    
## <a name="see-also"></a>Confira também



[Fluxo de preenchimento automático](autocomplete-stream.md)
  
[Perfis MAPI](mapi-profiles.md)


[Outlook 2003/2007 NK2 de formato de arquivo e diretrizes para desenvolvedores](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)


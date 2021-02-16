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
  
O Microsoft Office Outlook 2007, o Microsoft Outlook 2010 e o Microsoft Outlook 2013 interagem com o cache de apelidos, também conhecido como "fluxo de preenchimento automático". O fluxo de preenchimento automático é onde o Outlook mantém a lista de preenchimento automático, que é a lista de nomes que é exibida nas caixas de edição **Para**, **Cc** e **Cc** enquanto um usuário está compondo um email. Este tópico descreve como o Outlook 2007, o Outlook 2010 e o Outlook 2013 interagem com o fluxo de preenchimento automático e também discute o formato binário do arquivo e as maneiras recomendadas para interagir com o fluxo de preenchimento automático. 
  
Para aplicativos que interagem com o Outlook 2010 ou o Outlook 2013, o fluxo de preenchimento automático é armazenado como uma propriedade MAPI e pode ser modificado usando o MAPI ou o objeto **PropertyAccessor** da mensagem. O **objeto PropertyAccessor** é exposto nos modelos de objeto do Outlook 2010 ou do Outlook 2013. 
  
Não há dependências no modelo de objeto do Outlook 2007 ou APIs MAPI. Portanto, os aplicativos que fazem alterações no fluxo de preenchimento automático no Outlook 2007 podem ser escritos usando qualquer linguagem de programação.
  
## <a name="interacting-with-the-autocomplete-stream"></a>Interagindo com o fluxo de preenchimento automático

Quando as **caixas de** edição Para , **Cc** ou **Cc** são acessadas em uma mensagem, o fluxo de preenchimento automático é carregado e a lista de nomes de usuário é exibida. O Outlook interage com o fluxo de preenchimento automático de duas maneiras: 
  
1. Carregando o fluxo de preenchimento automático 
    
2. Salvando alterações nos dados no fluxo de preenchimento automático
    
O meio de armazenar os dados de preenchimento automático difere entre o Outlook 2007 e o Outlook 2010 ou o Outlook 2013 da seguinte maneira: 
  
 **Outlook 2007**
  
Para o Outlook 2007, o fluxo de preenchimento automático é armazenado em um arquivo com o mesmo nome do perfil e uma extensão de .nk2. Por exemplo, se o perfil padrão "outlook" for usado, o arquivo será chamado de "outlook.nk2". O arquivo .nk2 é armazenado em %APPDATA%\Microsoft\Outlook. Para obter mais informações sobre o formato de arquivo binário de cache de apelidos, consulte [Outlook 2003/2007 NK2 File Format and Developer Guidelines](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).
  
 **Outlook 2010 e Outlook 2013**
  
Outlook 2010 or Outlook 2013 reads the autocomplete stream from a message in the Associated Contents table of the Inbox of the mail account's delivery store. Essa mensagem oculta tem uma classe de mensagem e um assunto IPM.Configuration. Preenchimento automático. O fluxo de preenchimento automático é armazenado nessa mensagem na propriedade PR_ROAMING_BINARYSTREAM ([propriedade canônica PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)). Os dados de preenchimento automático podem ser temporariamente armazenados em cache em um arquivo .dat de preenchimento automático localizado em %USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache. No entanto, o arquivo .dat é apenas um cache e não é usado para gravar de volta no armazenamento de entrega quando o usuário sai do Outlook 2010 ou do Outlook 2013.
  
## <a name="loading-the-autocomplete-stream"></a>Carregando o fluxo de preenchimento automático

O Outlook carrega o fluxo de preenchimento automático sempre que um item com a funcionalidade de endereçamento é inicializado. Por exemplo, os endereços de email são usados em um novo email, uma resposta de email, um item de contato, uma solicitação de reunião e assim por diante. Para carregar os dados, o Outlook lê todo o conteúdo do fluxo na memória.
  
Para operações de preenchimento automático, o Outlook interage exclusivamente com essa estrutura na memória pela duração do tempo outlook.exe tempo de vida do processo. O Outlook só salva a estrutura no desligamento. Consulte a seção a seguir "Salvando o fluxo de preenchimento automático" para obter mais informações sobre esse processo.
  
## <a name="saving-the-autocomplete-stream"></a>Salvando o fluxo de preenchimento automático

Outlook saves the autocomplete stream on shutdown if the autocomplete list has changed in any of the following ways:
  
- Uma nova entrada de apelido é adicionada por meio da resolução de um nome, da escolha de um destinatário na caixa de diálogo do livro de endereços ou do envio de email para um destinatário que ainda não estava na lista.
    
- Uma entrada é modificada pelo envio de email para um destinatário existente na lista.
    
- Uma entrada é removida pelo usuário por meio da interface do usuário.
    
- Outros cenários secundários não relevantes para este tópico.
    
Salvar alterações nos dados de preenchimento automático envolve escrever a estrutura na memória de volta para um [fluxo de preenchimento automático.](autocomplete-stream.md) Ao interagir com o Outlook 2007, o fluxo é salvo em um arquivo .nk2 local. Para o Outlook 2010 ou o Outlook 2013, o fluxo de preenchimento automático grava de volta na tabela Conteúdo Associado da Caixa de Entrada do armazenamento de entrega da conta de email.
  
## <a name="recommendations"></a>Recomendações

- Nunca modifique parcialmente o fluxo de preenchimento automático. A interação com suporte é para 1) ler todo o fluxo de preenchimento automático na memória, 2) modificar a estrutura de memória e 3) gravar todo o fluxo de volta na tabela Conteúdo Associado da Caixa de Entrada do armazenamento de entrega da conta de email (para Outlook 2010 ou Outlook 2013) ou para o arquivo .nk2 local (Outlook 2007).
    
- Não interaja com o fluxo de preenchimento automático enquanto o Outlook estiver em execução. Se o Outlook estiver em execução enquanto você modifica o fluxo, ele provavelmente substituirá suas alterações quando for desligado.
    
- Não escreva propriedades do tipo PT_MV_UNICODE e PR_MV_STRING8 em um fluxo de preenchimento automático a ser consumido pelo Microsoft Outlook 2003. Essas propriedades só são compreendidas pelo Outlook 2007, Outlook 2010 e Outlook 2013.
    
- Ao desenvolver código que interage com o Outlook 2007, recomendamos que você bloqueie a modificação do arquivo .nk2 por outros processos enquanto você o lê e escreve usando APIs de bloqueio de arquivo padrão (por exemplo, **LockFile** em C/C++ e **FileStream.Lock** em C#). 
    
- Somente modifique as propriedades dos tipos que são do conjunto de linhas do fluxo de preenchimento automático. Para obter mais informações sobre as propriedades de fluxo de preenchimento automático e os tipos de propriedade, consulte [Autocomplete Stream](autocomplete-stream.md).
    
## <a name="see-also"></a>Confira também



[Fluxo de Preenchimento Automático](autocomplete-stream.md)
  
[Perfis MAPI](mapi-profiles.md)


[Outlook 2003/2007 NK2 File Format and Developer Guidelines](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)


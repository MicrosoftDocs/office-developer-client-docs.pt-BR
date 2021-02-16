---
title: Endereços únicos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9224c694-b26f-42c7-9404-ee2dd832cfbb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e6bda55951d8df5c5da272750c631ec105b2ccf2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409108"
---
# <a name="one-off-addresses"></a>Endereços únicos

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Endereços one-off são usados para enviar mensagens a destinatários one-off, destinatários que não têm uma entrada correspondente em nenhum dos contêineres do livro de endereços da sessão. Os clientes podem criar endereços único quando adicionam novas entradas ao livro de endereços ou novos destinatários à lista de destinatários de uma mensagem de saída. Endereços one-off podem ser adicionados a qualquer contêiner que seja modificável.
  
Para criar um endereço único, os clientes usam um modelo especial contendo controles de edição para inserir todas as informações que comitam um endereço único. Endereços one-off, como endereços de outros tipos, usam um formato predefinido. O formato de endereço único é definido pelo MAPI da seguinte forma:
  
`Display name[Address type:Email address]`
  
Há seis componentes para esse formato e algumas regras sobre caracteres fictícios. Os componentes são descritos na tabela a seguir.
  
|**Componente**|**Uso**|**Descrição**|
|:-----|:-----|:-----|
|Nome de exibição  <br/> |Opcional  <br/> |Se não estiver presente, **IAddrBook::ResolveName** usará a parte visível do endereço de email como o nome de exibição. Pode incluir espaços em branco. Para obter mais informações, consulte [IAddrBook::ResolveName](iaddrbook-resolvename.md).  <br/> |
|[  <br/> |Obrigatório  <br/> |Delineia o início das informações de tipo e endereço.  <br/> |
|]  <br/> |Obrigatório  <br/> |Delineia o final das informações de tipo e endereço. Se algo diferente do espaço em branco seguir esse caractere, a entrada não será tratada como um destinatário personalizado.  <br/> |
|Tipo de endereço  <br/> |Obrigatório  <br/> |Tipo de endereço; mapeia para um formato de endereço específico. Para obter mais informações, consulte [MAPI Address Types](mapi-address-types.md).  <br/> |
|:  <br/> |Obrigatório  <br/> |Separa o tipo de endereço do endereço de email.  <br/> |
|Email  <br/> |Obrigatório  <br/> |Endereço do destinatário. Pode incluir espaços em branco.  <br/> |
   
MAPI uses particular sets of characters characters to allow addresses to contain special characters such as comma (,), left bracket ([) and colon (:) e alguns caracteres não impríveis, como o retorno de carro ou alimentação de linha ou qualquer outro equivalente hexadecimal. O caractere de ataque é a invertida ( \) . Portanto, se os clientes ou provedores deverão inserir uma invertida em um endereço, eles deverão pré-colocar em pré-rede o caractere de ataque (" \\ ").
  
Os clientes e provedores de serviços podem usar essa técnica de técnica de técnica em qualquer um dos campos não corrigidos e digitáveis. Por exemplo, a entrada a seguir é traduzida para Bill Lee como o nome para exibição, MSPEER como o tipo de endereço e \\ billll\in como o endereço de email:
  
`Bill Lee[MSPEER:\\\\billl\in]`

Para inserir caracteres especiais não digitáveis, os clientes e provedores de serviços usam um caractere de inserção seguido por um x e dois dígitos hexadecimais para representar seu equivalente hexadecimal. Por exemplo, se um endereço tiver um caractere não digitar que equivale a um retorno de carro, (\0d) em hexadecimal, um cliente o digitará como:
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

**IAddrBook::ResolveName** também analisará automaticamente a maioria dos endereços SMTP, procurando endereços com o seguinte formato: 
  
`XXX@YYY.ZZZ`

Embora nem todos os formatos RFC822 possíveis sejam tratados, essa análise automática é adequada para a maioria dos usuários. **O ResolveName** inclui essa funcionalidade para permitir que os usuários insiram endereços SMTP diretamente em uma mensagem e que essa mensagem vá para o usuário da Internet. Os componentes XXX, AAA e ZZZ do endereço podem ter um ou mais caracteres. O sinal de acinzeira (@) não pode ser incluído nos componentes de endereço XXX, AAA ou ZZZ e o componente AAA também não pode incluir o ponto. Como os seguintes caracteres são caracteres especiais em endereços SMTP, MAPI converte automaticamente um nome de exibição contendo esses caracteres em um endereço único: 
  
- \>\>
    
- @
    
- \<\>
    
- .
    
Cada endereço único recebe um identificador de entrada único correspondente. Para fazer essa atribuição, os clientes chamam **IAddrBook::CreateOneOff** e os provedores de transporte chamam **IMAPISupport::CreateOneOff**. Para obter mais informações, [consulte IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) e [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Ao processar mensagens de entrada, os provedores de transporte criam identificadores de entrada único para endereços de gateway e para endereços que não podem ser manipulados pelos provedores de agendamento associados ao transporte. Os provedores de transporte verificam o tipo de cada endereço em uma mensagem para determinar se ele pode ser manipulado por um provedor de agendas associado ao transporte. Se não puder, os provedores de transporte **chamarão IMAPISupport::CreateOneOff** para associar o endereço a um identificador de entrada único. 
  
Os identificadores de entrada único incluem as seguintes informações na seguinte ordem:
  
1. **MAPIUID**
    
2. Versão
    
3. Sinalizadores
    
4. Nome de exibição
    
5. Tipo de endereço
    
6. Email
    
Nas chamadas para **IAddrBook::CreateOneOff** e **IMAPISupport::CreateOneOff**, os clientes e provedores de transporte podem definir um sinalizador que indica se o destinatário representado pelo endereço único pode ou não processar texto formatado ou objetos OLE incorporados. Para indicar que um destinatário pode manipular texto formatado e objetos OLE, os clientes e provedores de transporte configuram o MAPI_SEND_NO_RICH_INFO de texto no _parâmetro ulFlags._ MAPI then sets the one-off recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE. Quando esse sinalizador não estiver  definido, o MAPI PR_SEND_RICH_INFO como VERDADEIRO, a menos que o endereço único seja interpretado como um endereço SMTP. Nesse caso, o **PR_SEND_RICH_INFO** padrão é FALSE. 
  
## <a name="see-also"></a>Confira também

- [IAddrBook::ResolveName](iaddrbook-resolvename.md)


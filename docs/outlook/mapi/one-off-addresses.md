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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279633"
---
# <a name="one-off-addresses"></a>Endereços únicos

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os endereços únicos são usados para enviar mensagens para destinatários únicos, destinatários que não têm uma entrada correspondente em qualquer um dos contêineres do catálogo de endereços da sessão. Os clientes podem criar endereços únicos ao adicionar novas entradas ao catálogo de endereços ou a novos destinatários à lista de destinatários de uma mensagem de saída. Endereços únicos podem ser adicionados a qualquer contêiner modificável.
  
Para criar um endereço one-off, os clientes usam um modelo especial contendo controles de edição para inserir todas as informações que compõem um endereço one-off. Endereços únicos, como endereços de outros tipos, usam um formato predefinido. O formato de endereço one-off é definido por MAPI da seguinte maneira:
  
`Display name[Address type:Email address]`
  
Há seis componentes para este formato e algumas regras sobre a cotação de caracteres. Os componentes são descritos na tabela a seguir.
  
|**Componente**|**Usage**|**Descrição**|
|:-----|:-----|:-----|
|Nome diferenciado (DN)  <br/> |Opcional  <br/> |Se não estiver presente, **IAddrBook:: resolvedor** usa a parte visível do endereço de email como o nome de exibição. Pode incluir espaços em branco. Para obter mais informações, consulte [IAddrBook:: ResolveName](iaddrbook-resolvename.md).  <br/> |
|[  <br/> |Obrigatório  <br/> |Delineia o início das informações de tipo e endereço.  <br/> |
|]  <br/> |Obrigatório  <br/> |Delineia o final das informações de tipo e endereço. Se algo diferente de espaço em branco seguir esse caractere, a entrada não será tratada como um destinatário personalizado.  <br/> |
|Tipo de endereço  <br/> |Obrigatório  <br/> |Tipo de endereço; mapeia para um formato de endereço específico. Para obter mais informações, consulte [tipos de endereço MAPI](mapi-address-types.md).  <br/> |
|:  <br/> |Obrigatório  <br/> |Separa o tipo de endereço do endereço de email.  <br/> |
|Endereço de email  <br/> |Obrigatório  <br/> |Endereço do destinatário. Pode incluir espaços em branco.  <br/> |
   
O MAPI usa conjuntos específicos de caracteres de cotação para permitir que os endereços contenham caracteres especiais, como vírgula (,), colchete esquerdo ([) e dois-pontos (:) e alguns caracteres não typeáveis como o retorno de carro ou alimentação de linha ou qualquer outro equivalente hexadecimal. O caractere quot é a barra invertida (\). Portanto, se os clientes ou provedores precisarem inserir uma barra invertida em um endereço, eles devem preceder com o caractere\\de quot ("").
  
Os clientes e provedores de serviços podem usar essa técnica de cotação em qualquer um dos campos não fixos e de tipo. Por exemplo, a seguinte entrada é traduzida como Bill lontra como o nome de exibição, MSPEER como o tipo de endereço \\e billll\in como o endereço de email:
  
`Bill Lee[MSPEER:\\\\billl\in]`

Para inserir caracteres especiais não digitados, os clientes e provedores de serviços usam um caractere de cotação seguido por um x e dois dígitos hexadecimais para representar seus equivalentes hexadecimais. Por exemplo, se um endereço tiver um caractere que não possa ser digitado que seja igual a um retorno de carro, (\0d) em hexadecimal, um cliente o inserirá como:
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

**IAddrBook:: resolvedor** também analisa automaticamente a maioria dos endereços SMTP, procurando endereços com o seguinte formato: 
  
`XXX@YYY.ZZZ`

Embora nem todos os formatos de RFC822 possíveis sejam tratados, essa análise automática é adequada para a maioria dos usuários. **** O resolvedor inclui essa funcionalidade para permitir que os usuários insiram endereços SMTP diretamente em uma mensagem e que a mensagem vá para o usuário da Internet. Os componentes XXX, YYY e ZZZ do endereço podem ser um ou mais caracteres. O sinal de arroba (@) não pode ser incluído nos componentes de endereço XXX, YYY ou ZZZ e o componente YYY também não pode incluir o ponto. Como os caracteres a seguir são caracteres especiais em endereços SMTP, o MAPI converte automaticamente um nome de exibição que contém esses caracteres em um endereço one-off: 
  
- \>\>
    
- @
    
- \<\>
    
- .
    
Cada endereço one-off é atribuído a um identificador de entrada único correspondente. Para fazer essa atribuição, os clientes chamam **IAddrBook:: CreateOneOff** e provedores de transporte chamam **IMAPISupport:: CreateOneOff**. Para obter mais informações, consulte [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) e [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md). Ao processar mensagens de entrada, os provedores de transporte criam identificadores de entrada únicos para endereços de gateway e para endereços que não podem ser manipulados pelos provedores de catálogo de endereços associados do transporte. Os provedores de transporte verificam o tipo de cada endereço em uma mensagem para determinar se ele pode ser manipulado por um provedor de catálogo de endereços associado ao transporte. Se não puder, os provedores de transporte chamarão **IMAPISupport:: CreateOneOff** para associar o endereço a um identificador de entrada one-off. 
  
Os identificadores de entrada únicos incluem as seguintes informações na seguinte ordem:
  
1. **MAPIUID**
    
2. Version
    
3. Sinalizadores
    
4. Nome diferenciado (DN)
    
5. Tipo de endereço
    
6. Endereço de email
    
Nas chamadas para **IAddrBook:: CreateOneOff** e **IMAPISupport:: CreateOneOff**, os clientes e provedores de transporte podem definir um sinalizador que indica se o destinatário representado ou não pelo endereço one-off pode processar texto formatado ou OLE incorporado objectos. Para indicar que um destinatário pode manipular texto formatado e objetos OLE, os clientes e provedores de transporte definem o sinalizador MAPI_SEND_NO_RICH_INFO no parâmetro _parâmetroulflags_ . MAPI define a propriedade **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) do destinatário única como false. Quando esse sinalizador não é definido, MAPI define **PR_SEND_RICH_INFO** como true, a menos que o endereço one-off seja interpretado como um endereço SMTP. Nesse caso, **PR_SEND_RICH_INFO** padrão é false. 
  
## <a name="see-also"></a>Confira também

- [IAddrBook::ResolveName](iaddrbook-resolvename.md)


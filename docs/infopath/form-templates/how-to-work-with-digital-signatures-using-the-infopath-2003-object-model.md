---
title: Trabalhar com assinaturas digitais usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- assinaturas digitais [InfoPath 2007], modelos de formulário compatíveis com o InfoPath 2003, modelos de formulário compatíveis com o InfoPath 2003, assinaturas digitais
localization_priority: Normal
ms.assetid: d6318238-fd45-4854-a3c9-c27c5685bd6b
description: O modelo de objeto compatível com o InfoPath 2003 fornece recursos para trabalhar com assinaturas digitais programaticamente.
ms.openlocfilehash: 86e2c85c7515c896612df09b6186462480ceff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433441"
---
# <a name="work-with-digital-signatures-using-the-infopath-2003-object-model"></a>Trabalhar com assinaturas digitais usando o modelo de objeto do InfoPath 2003

O modelo de objeto compatível com o InfoPath 2003 fornece recursos para trabalhar com assinaturas digitais programaticamente.
  
## <a name="digital-signature-features"></a>Recursos de assinatura digital

Os recursos de assinaturas digitais disponíveis no InfoPath permitem: 
  
- Habilitar assinaturas para o formulário inteiro ou para conjuntos específicos de dados no formulário que podem ser assinados separadamente.
    
- Especifique, para cada conjunto de dados que podem ser assinados, se uma assinatura única ou várias assinaturas são permitidas e qual será a relação. Por exemplo, você pode especificar se são assinaturas paralelas ou se cada nova assinatura assina todas as assinaturas anteriores.
    
- Especifique uma mensagem a ser mostrada para os usuários de forma que eles assinem o formulário.
    
- Insira e veja uma assinatura no documento. 
    
- Exibir informações verificáveis de não repúdio que foram adicionadas a cada assinatura para aumentar a segurança. Essas informações adicionais, que incluem um modo de exibição do formulário como foram apresentadas a cada signatário, fazem parte da assinatura e não podem ser removidas sem invalidar a assinatura. A qualquer momento, você pode recuperar esses dados clicando na assinatura no formulário para exibir a caixa de diálogo **verificar assinatura digital** . 
    
- Aproveite um modelo de objeto para trabalhar com assinaturas digitais. Adicione informações personalizadas ao bloco de assinatura em formulários totalmente confiáveis por meio do modelo de objeto de assinatura digital. 
    
## <a name="overview-of-the-digital-signatures-object-model"></a>Visão geral do modelo de objeto de assinaturas digitais

### <a name="events"></a>Eventos

O modelo de objeto para assinaturas digitais fornece o seguinte evento.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx) <br/> |Ocorre após um conjunto de dados assináveis ter sido selecionado para assinar.  <br/> Você pode usar esse evento para manipular os dados armazenados na assinatura digital. Por exemplo, você pode adicionar dados de um servidor de carimbo de data/hora confiável ou adicionar uma referenda do lado do servidor da transação. Você também pode usar esse evento para bloquear a assinatura se o usuário atual não for um membro de um grupo específico.  <br/> |
   
O **** evento OnSign retorna uma referência ao objeto [SignEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEventObject.aspx) , que fornece as propriedades a seguir. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[ReturnStatus](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.ReturnStatus.aspx) <br/> |Obtém ou define um valor **Boolean** que indica o status de retorno do evento OnSign. ****  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SignEvent.SignedDataBlock.aspx) <br/> |Obtém o bloco de dados assinado que disparou **** o evento OnSign.  <br/> |
|[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignEvent.XDocument.aspx) <br/> |Obtém uma referência ao objeto **XDocument** associado ao evento **OnSign** .  <br/> |
   
### <a name="collections-and-objects"></a>Coleções e objetos

O modelo de objeto para assinaturas digitais fornece as seguintes coleções.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[SignedDataBlocksCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlocksCollection.aspx) <br/> |A coleção dos objetos [SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) no modelo de formulário, conforme definido no arquivo de definição de formulário (. xsf).  <br/> A coleção **SignedDataBlocksCollection** implementa propriedades que podem ser usadas para acessar os objetos **SignedDataBlockObjects** associados a um formulário. A coleção **SignedDataBlocks** é acessível através da propriedade [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SignedDataBlocks.aspx) do objeto [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) .  <br/> |
|[Signaturecollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignaturesCollection.aspx) <br/> |Contém uma coleção de [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) objetos signatureobject para cada **SignedDataBlockObject** no formulário.  <br/> A **** coleção signaturecollection implementa propriedades e um método que pode ser usado para acessar os objetos signatureobject **** associados de um formulário e para criar uma assinatura. Ele pode ser acessado através do objeto **SignedDataBlockObject** .  <br/> Quando você usa o método [Create](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signatures.Create.aspx) da coleção **signaturecollection** , tenha em mente que a assinatura não é gravada até que o método [signobject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) seja chamado no objeto **signatureobject** . Esses métodos podem ser chamados apenas do manipulador **** de eventos OnSign de um modelo de formulário totalmente confiável.  <br/> |
   
O modelo de objeto para assinaturas digitais fornece os seguintes objetos.
  
|**Nome**|**Descrição**|
|:-----|:-----|
|[SignedDataBlockObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignedDataBlockObject.aspx) <br/> |Representa um conjunto de dados assináveis em um formulário. O objeto **signedDataBlock** fornece várias propriedades e um método que pode ser usado para interagir programaticamente com um conjunto de dados assináveis.  <br/> |
|[Signatureobject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SignatureObject.aspx) <br/> |Representa uma assinatura digital que foi adicionada a um formulário ou a um conjunto de dados assináveis em um formulário. A **** coleção signatureobject implementa propriedades que podem ser usadas para recuperar informações sobre a assinatura digital e o método [Sign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Signature.Sign.aspx) para gravar o bloco de assinatura digital XML e a computação de seu valor de hash criptográfico.  <br/> |
|[CertificateObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.CertificateObject.aspx) <br/> |Representa o certificado digital X. 509 que foi usado para criar a assinatura.  <br/> |
   
## <a name="working-with-digital-signatures-programmatically"></a>Trabalhar com assinaturas digitais de forma programática

O modelo de objeto compatível com o InfoPath 2003 fornece membros para interagir com assinaturas digitais programaticamente. Em particular, os formulários totalmente confiáveis podem adicionar informações personalizadas ao bloco de assinatura antes de serem confirmadas, de acordo com a seguinte linha do tempo:
  
1. O usuário opta por adicionar uma assinatura digital a um formulário.
    
2. O primeiro painel do **Assistente de assinatura digital** é exibido. 
    
3. O **** evento OnSign para os dados selecionados representado pelo objeto **SignedDataBlockObject** é gerado e o método **Sign** de **SignedDataBlockObject** e o método **Create** de **signaturecollection** coleção são executadas. 
    
4. Qualquer ação personalizada opcional é executada.
    
5. O método **Sign** de **signatureobject** é executado. 
    
6. O segundo e terceiro painéis do assistente são exibidos para selecionar um certificado para entrar e inserir comentários.
    
7. As informações de não repúdio são exibidas (o que pode ser exibido posteriormente com a caixa de diálogo **verificar assinatura digital** ). 
    
8. Quando o botão de **sinal** é clicado, a assinatura é adicionada à coleção de assinaturas para o formulário. 
    
O exemplo a seguir chama a caixa de diálogo **assinar** e referenda a assinatura com um valor de carimbo de data/hora recuperado de um serviço de carimbo de data/hora confiável. 
  
```cs
[InfoPathEventHandler(EventType=InfoPathEventType.OnSign)]
public void OnSign(SignEvent e)
{
    Signature signature = e.SignedDataBlock.Signatures.Create();
    // Invoke the Sign dialog box to sign the data block.
    signature.Sign();
    // Countersign the signature with a trusted timestamp
    // Get the XML node storing the signature block
    IXMLDOMNode oNodeSig = signature.SignatureBlockXmlNode;
    IXMLDOMNode oNodeSigValue = oNodeSig.selectSingleNode(".//*[local-name(.)='signatureValue']");
    // Get timestamp from a trusted timestamp service (fictitious).
    MyTrustedTimeStampService s = new MyTrustedTimeStampService();
    string strVerifiedTimeStamp = s.AddTimeStamp(oNodeSigValue.text);
    
    //Add the value returned from the timestamp service to the 
    //unsigned part of the signature block
    IXMLDOMNode oNodeObj = oNodeSig.selectSingleNode(".//*[local-name(.)='Object']");
    IXMLDOMNode oNode = oNodeObj.cloneNode(false);
    oNode.text = strVerifiedTimeStamp;
    oNodeObj.parentNode.appendChild(oNode);
    e.ReturnStatus = true;
}
```



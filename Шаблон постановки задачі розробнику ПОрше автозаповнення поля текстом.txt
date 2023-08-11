function setValueAttr(code, value) {
  const attr = EdocsApi.getAttributeValue(code);
  attr.value = value;
  EdocsApi.setAttributeValue(attr);
}

function setcountry() {
  const travelDirection = EdocsApi.getAttributeValue("travelDirection").value;
  if (travelDirection && travelDirection == "Україна") {
    setValueAttr("country", travelDirection);
  } else {
    setValueAttr("country", null);
  }
}

function onChangetravelDirection() {
  setcountry();
}

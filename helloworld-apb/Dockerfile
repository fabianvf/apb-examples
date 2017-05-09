FROM ansibleplaybookbundle/apb-src-base
# MAINTAINER {{ $MAINTAINER }}

LABEL "com.redhat.apb.version"="0.1.0"
LABEL "com.redhat.apb.spec"=\
"aWQ6IGYzMmRlM2JjLTMyMjUtNDI5YS1iMjNiLWNlZjQ3Y2ExZDI1YwpuYW1lOiBoZWxsb3dvcmxk\
LWFwYgppbWFnZTogamtpZy9oZWxsb3dvcmxkLWFwYgpkZXNjcmlwdGlvbjogSGVsbG8gV29ybGQg\
d2l0aCBOR0lOWCBhcGIKYmluZGFibGU6IHRydWUKYXN5bmM6ICJvcHRpb25hbCIKcGFyYW1ldGVy\
czoKICAtIG5hbWU6IHByb2plY3RfbmFtZQogICAgZGVzY3JpcHRpb246IE5hbWVzcGFjZSB0byBk\
ZXBsb3kgY29udGFpbmVycyB0bwogICAgZGVmYXVsdDogaGVsbG93b3JsZC1hcGIKICAtIG5hbWU6\
IHNlc3Npb25fa2V5CiAgICBkZXNjcmlwdGlvbjogS2V5IGZvciByZWNvdmVyaW5nIHNlc3Npb24u\
IFdpbGwgZGVmYXVsdCB0byByYW5kb20gVVVJRAogICAgZGVmYXVsdDogdGVzdAogICAgcmVxdWly\
ZWQ6IGZhbHNlCg=="

ADD playbooks /opt/apb/actions
ADD roles /opt/ansible/roles

RUN useradd -u 1001 -r -g 0 -M -b /opt/apb -s /sbin/nologin -c "apb user" apb
RUN chown -R 1001:0 /opt/apb
USER 1001

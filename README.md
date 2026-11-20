# AWS Terraform Lab: Break It, Fix It, Document It

A hands-on lab for building cloud support and operations skills. I build a small AWS environment with Terraform, deliberately break it, and write an incident note for each issue.

**Status: in progress.** Nothing below is finished until it is checked off.

## Planned environment
- [ ] VPC with a public subnet, internet gateway, and route table
- [ ] One small EC2 instance running a simple web server, behind a security group
- [ ] CloudWatch alarm with an SNS email notification

## Planned break/fix scenarios
Each scenario gets its own runbook in the `runbooks/` folder.
- [ ] Security group blocks port 80
- [ ] Missing route to the internet gateway
- [ ] Web server service stopped on the instance

## Runbook format
Every incident note follows the same structure:
1. **Symptom:** what the user or alarm reported
2. **Investigation:** the steps and checks I ran, in order
3. **Root cause:** what was actually wrong
4. **Fix:** what I changed
5. **Prevention:** how to avoid or catch it earlier

## Tools
AWS (VPC, EC2, CloudWatch, SNS), Terraform, Linux

## Cost and safety
- Resources are small and destroyed with `terraform destroy` after each session.
- No credentials, account IDs, or state files are committed to this repo.

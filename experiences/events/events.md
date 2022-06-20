# JavaScript API Events

Through LoyJoy [JavaScript API](/experiences/publish/javascript_api/javascript_api.md) following events are emitted automatically for the various process modules in the chat. Typically each event is prefixed with the name of the process module, e.g. event `birthdate_entered` for the [Birthdate process module](/help/processes/process/subprocesses/birthdate/birthdate.md).

The following list covers most process modules and events. Please note that:
- the event names do not form a forever constant API, as they may be extended and changed with the further development and growing feature set of LoyJoy Cloud Platform.
- additional event names that are not included in this list may be emitted by the [JavaScript API](/experiences/publish/javascript_api/javascript_api.md), as with the [Event process module](/help/processes/process/subprocesses/event/event.md) custom events can be defined and emitted by the modeller




| Event name          | Event description |
|---------------------|------------------|
| hide                | The chat window was not displayed when loading or hidden (hidden) after loading via JavaScript API. |
| load                | The chat was loaded. |
| open                | The chat was opened. |
| show                | The chat was displayed / no longer hidden. |
|-- |-- |
| advent_calendar_door_asked | A customer was asked whether to open an advent calendar door. |
| advent_calendar_door_opened | A customer has confirmed to open an advent calendar door. |
| appointment_created | An appointment was created in the appointment process module. |
| audio_message_requested | A customer was asked to record an audio message in the audio message process module. |
| audio_message_uploaded | A customer has uploaded an audio message in the audio message process module. |
| beiersdorf_api_post_consumers_subscription | A newsletter subscription as defined in the according process module has been written into a consumer profile (Consumer without first name, last name, password) |
| beiersdorf_api_post_users_care_profile | Skin type data as defined in the according process module has been written to user care profile |
| beiersdorf_api_post_users_channel_permissions | Channel permission as defined in the according process module such as for email, ads, social etc. has been written to user |
| beiersdorf_api_post_users_consents | Consent as defined in the according process module for a membership, subscription or channel permission has been written to user |
| beiersdorf_api_post_users_engagements | Engagement as defined in the according process module such as a participation has been written to user |
| beiersdorf_api_post_users_memberships | Membership in a customer program as defined in the according process module has been written to user |
| beiersdorf_api_post_users_profile | Data as defined in the according process module has been written to user profile |
| beiersdorf_api_post_users_subscriptions | A newsletter subscription as defined in the according process module has been written for a certain topic into a full user profile (User with first name, last name, password) |
| beiersdorf_api_put_users_password | Password has been written to user profile |
| beiersdorf_sign_in | A sign in via chat has happened |
| beiersdorf_sign_in_via_cookie | A sign in via cookie has happened |
| beiersdorf_sign_up | A sign up via chat has happened |
| beiersdorf_sign_up_requested | A sign up via chat has been requested, i.e. the sign-up form has been rendered |
| beiersdorf_verification_code_failed | A sign-in verification code has been entered, however validation failed, i.e. code was incorrect |
| beiersdorf_verification_code_succeeded | A sign-in verification code has been entered, and validation succeeded, i.e. code was correct |
| birthdate_entered | A customer has entered their birthday in the birthdate process module. |
| campaign_message_sent | A campaign message was sent. |
| code_entered | A customer has entered a code in the code process module. |
| code_entered_correct | A customer has entered a correct code in the code process module.  |
| code_entered_incorrect | A customer has entered an incorrect code in the code process module. |
| code_registered | A code entered by a customer was registered. |
| coupon_code_issued | A coupon code was issued to a customer in the coupon code process module. |
| coupon_code_uploaded | A coupon code was uploaded in the LoyJoy backend. |
| customer_created | A customer was created. |
| customer_deleted | A customer was deleted. |
| customer_purged | Customers were purged in the LoyJoy backend. |
| customer_updated | A customer was updated, e.g. by entering personal information such as name or birthdate. |
| data_collection_answer | A user has given a pre-defined answer in a questionnaire process module (this includes e.g. quick reply type questions, but not text type). |
| data_collection_answer_idontknow | A user has clicked the "I don't know option" in an questionnaire. |
| data_collection_nps_survey_score_0 | A customer has given the score of 0 in the NPS question type of the questionnaire |
| data_collection_nps_survey_score_1 | A customer has given the score of 1 in the NPS question type of the questionnaire |
| data_collection_nps_survey_score_10 | A customer has given the score of 10 in the NPS question type of the questionnaire |
| data_collection_nps_survey_score_2 | A customer has given the score of 2 in the NPS question type of the questionnaire |
| data_collection_nps_survey_score_3 | A customer has given the score of 3 in the NPS question type of the questionnaire |
| data_collection_nps_survey_score_4 | A customer has given the score of 4 in the NPS question type of the questionnaire |
| data_collection_nps_survey_score_5 | A customer has given the score of 5 in the NPS question type of the questionnaire |
| data_collection_nps_survey_score_6 | A customer has given the score of 6 in the NPS question type of the questionnaire |
| data_collection_nps_survey_score_7 | A customer has given the score of 7 in the NPS question type of the questionnaire |
| data_collection_nps_survey_score_8 | A customer has given the score of 8 in the NPS question type of the questionnaire |
| data_collection_nps_survey_score_9 | A customer has given the score of 9 in the NPS question type of the questionnaire |
| data_collection_question | A question was asked in a questionnaire.  |
| data_collection_question_answered | A question was answered in a questionnaire (this includes all question types). |
| data_collection_variable_set | A variable was set in a questionnaire. |
| end | The end of a process / chat flow was reached. |
| firstname_entered | A customer has entered their first name in a firstname process module. |
| gender_diverse | A customer has entered their gender as diverse in a gender process module. |
| gender_entered | A customer has entered their gender in a gender process module. |
| gender_female | A customer has entered their gender as female in a gender process module. |
| gender_male | A customer has entered their gender as male in a gender process module. |
| handover_email_sent | A handover email was sent. |
| home_view_opened | The home view was opened (non-unique). |
| home_view_screen_time | 15 seconds of screen time were reached in a home view (iterative). |
| intent_evaluated | An intent was evaluated (i.e. a user has entered free text). |
| intent_matched | A matching intent (above threshold) was found when evaluating intents. |
| interaction | A customer has interacted for the first time in a process / experience, i.e. has manually typed something in the chat, clicked an element in the chat etc. |
| jump_auto | An automatic jump process module was executed. |
| jump_decision_question | The question where to jump was asked in a jump decision process module. |
| jump_decision_1 | The preceeding jump_decision_question was ansered with the 1st option |
| jump_decision_2 | The preceeding jump_decision_question was ansered with the 2nd option |
| jump_decision_3 | The preceeding jump_decision_question was ansered with the 3rd option |
| jump_decision_4 | The preceeding jump_decision_question was ansered with the 4th option |
| jump_decision_5 | The preceeding jump_decision_question was ansered with the 5th option |
| jump_decision_6 | The preceeding jump_decision_question was ansered with the 6th option |
| jump_decision_7 | The preceeding jump_decision_question was ansered with the 7th option |
| jump_persistent_1 | The 1st persistent jump quick-reply was clicked |
| jump_persistent_2 | The 2nd persistent jump quick-reply was clicked |
| jump_persistent_3 | The 3rd persistent jump quick-reply was clicked |
| jump_persistent_4 | The 4th persistent jump quick-reply was clicked |
| jump_persistent_5 | The 5th persistent jump quick-reply was clicked |
| lastname_entered | A customer has entered their last name in a lastname process module. |
| link_clicked | A link was clicked in a external link or product gallery process module. |
| live_chat_duration | A certain duration was reached during a live chat. |
| live_chat_ended | A live chat was ended. |
| live_chat_started | A live chat was started. |
| loyalty_first_received | A customer has received their first loyalty points. |
| loyalty_points_emitted | Loyalty points were emitted to a customer. |
| loyalty_points_spent | A customer has spent loyalty points. |
| loyalty_referral | A customer has signed up after being referred by another customer via the loyalty referral process module. |
| loyalty_reward_redeemed | A customer has redeemed their loyalty points for a reward. |
| mail_sent | A mail was sent in the mail process module. |
| mail_to_customer_sent | A mail was sent in a mail to customer process module. |
| main_prize_sent | The main prize was shown in the main prize process module. |
| newsletter_double_opt_in | A customer has given the newsletter double opt-in via clicking the link in a double opt-in email. |
| newsletter_opt_out | A customer has opted out to newsletter via clicking the unsubscribe link in an email or the settings menu in chat. |
| newsletter_single_opt_in | A customer has given the newsletter single opt-in by agreeing in the chat. |
| newsletter_single_opt_in_asked | A customer was asked in chat whether they want to receive a newsletter. |
| newsletter_single_opt_in_rejected | A customer did not agree to receive the newsletter in chat. |
| nps_survey_free_text_answered | A customer has answered the text question in the NPS process module. |
| nps_survey_score_0 | A customer has given the score of 0 in the NPS process module. |
| nps_survey_score_1 | A customer has given the score of 1 in the NPS process module. |
| nps_survey_score_2 | A customer has given the score of 2 in the NPS process module. |
| nps_survey_score_3 | A customer has given the score of 3 in the NPS process module. |
| nps_survey_score_4 | A customer has given the score of 4 in the NPS process module. |
| nps_survey_score_5 | A customer has given the score of 5 in the NPS process module. |
| nps_survey_score_6 | A customer has given the score of 6 in the NPS process module. |
| nps_survey_score_7 | A customer has given the score of 7 in the NPS process module. |
| nps_survey_score_8 | A customer has given the score of 8 in the NPS process module. |
| nps_survey_score_9 | A customer has given the score of 9 in the NPS process module. |
| nps_survey_score_10 | A customer has given the score of 10 in the NPS process module. |
| participant_bpmn_process | A customer has participated for the first time in process / experience. |
| participant_giveaway | A customer has participated for the first time in a giveaway. |
| participation | A customer has participated in a giveaway. |
| password_entered | A customer has entered a password in the password process module. |
| phone_number_entered | A customer has entered their phone number in a phone number process module. |
| platform_facebook | A customer has chatted via Facebook messenger. |
| platform_rest | A customer has chatted via the chat UI on the website. |
| platform_viber | A customer has chatted via Viber. |
| platform_wechat | A customer has chatted via WeChat. |
| platform_whatsapp | A customer has chatted via WhatsApp. |
| postal_address_confirmed | A customer has confirmed the postal address they entered. |
| postal_address_updated | A customer has entered their postal address in a postal address process module. |
| prize_details_sent | A customer has requested the details for a prize in a prize process module. |
| prize_sent | A prize was sent in a prize process module. |
| proceed_confirmed | A customer has proceeded in a proceed process module. |
| process_liked | A customer has liked a process. |
| profiling_double_opt_in | A customer has given the profiling double opt-in via clicking the link in a double opt-in email. |
| profiling_opt_out | A customer has opted out to profiling via clicking the unsubscribe link in an email or the settings menu in chat. |
| profiling_single_opt_in | A customer has given the profiling single opt-in by agreeing in the chat. |
| profiling_single_opt_in_asked | A customer was asked in chat whether they agree to profiling. |
| profiling_single_opt_in_rejected | A customer did not agree to profiling in chat. |
| pub_sub_failed | A message to Pub/Sub could not be posted. |
| pub_sub_published | A message was posted to Pub/Sub in a Pub/Sub process module. |
| questionnaire_question | A question was asked in a questionnaire (legacy).  |
| quiz_answer | A customer has used a pre-defined answer in a quiz. |
| quiz_answer_correct | A customer has given a correct, pre-defined answer in a quiz. |
| quiz_answer_freetext | A customer has given a free text answer in a quiz. |
| quiz_answer_incorrect | A customer has given an incorrect, pre-defined answer in a quiz.  |
| quiz_answer_not_freetext | A customer has given a pre-defined answer in a quiz. |
| quiz_question | A question was asked in a quiz. |
| reminder_double_opt_in | A customer has given the reminder double opt-in via clicking the link in a double opt-in email. |
| reminder_opt_out | A customer has opted out to reminder via clicking the unsubscribe link in an email or the settings menu in chat. |
| reminder_single_opt_in | A customer has given the reminder single opt-in by agreeing in the chat. |
| reminder_single_opt_in_asked | A customer was asked in chat whether they agree to receive a reminder. |
| reminder_single_opt_in_rejected | A customer did not agree to receive a reminder in chat. |
| reset | A customer has triggered a chat reset. |
| restart | A customer has triggered a process re-start via the chat menu. |
| reward_redeemed | A customer has redeemed a reward in a rewards process module. |
| session_interacted | After a new chat session has started (cf. session_started), a customer has interacted for the first time in a process / experience, i.e. has manually typed something in the chat, clicked an element in the chat etc. |
| session_started | A customer has started a new chat session. A chat session starts as soon as a chat message occurs, either from a bot or a customer. It expires after 30 minutes of inactivity (cf. Google Analytics). |
| screen_time | Screen time was recorded in a chat. |
| sign_in | A customer has signed in. |
| sign_in_email_address_blocked | An email address was blocked because it was found on the block list for one-time email hosters.  |
| sign_in_ip_address_blocked | A customer was blocked from signing up because there were already too many sign ups from their IP address. |
| sign_in_pin_failed | A customer has entered an incorrect PIN / code when signing up / signing in. |
| sign_in_pin_mail_sent | A customer was sent an email with their PIN / code. |
| sign_in_pin_succeeded | A customer has entered a correct PIN / code when signing up / signing in. |
| sign_out | A customer has signed out via the chat menu. |
| sign_up | A new customer has signed up. |
| sign_up_requested | A customer was asked to sign up via entering the email address. |
| sms_double_opt_in | A customer has confirmed the text message double opt-in via entering the code they received via text. |
| sms_opt_in_code_sent | A customer has received a code via text in the text opt-in process module. |
| sms_single_opt_in | A customer has given the text single opt-in by agreeing in the chat. |
| sms_single_opt_in_asked | A customer was asked in chat whether they agree to receive text messages. |
| sms_single_opt_in_rejected | A customer did not agree to receive texts in chat. |
| snapshot_barcode_scanned | A customer has scanned a barcode in a snapshot process module. |
| snapshot_image_uploaded | A customer has uploaded an image in a snapshot process module. |
| start | A process was started. |
| story_read | A customer has read a story. |
| sub_process_visited | A sub process / process module was shown to a customer. |
| terms_accepted | A customer has accepted the experience / process terms. |
| terms_rejected | A customer has rejected the experience / process terms. |
| user_agent_desktop | A customer on a dektop computer has chatted. |
| user_agent_mobile | A customer on a mobile device has chatted. |
| variable_set | A variable was set in a variable process module. |
| web_push_double_opt_in | A customer has given the web-push double opt-in via agreeing to the question shown by their browser. |
| web_push_opt_in_subscription_request | A request was sent to a customer's browser to ask for web-push opt-in. |
| web_push_single_opt_in | A customer has given the web-push single opt-in by agreeing in the chat. |
| web_push_single_opt_in_asked | A customer was asked in chat whether they agree to receive web-push messages. |
| web_push_single_opt_in_rejected | A customer did not agree to receive web-push messages in chat. |
| web_push_subscription_gone | A customer's web-push subscription (handled by the browser) could not be found (was likely deleted by user). |
| reminder_opt_out | A customer has opted out to reminder via clicking the unsubscribe link in an email or the settings menu in chat. |
| reminder_single_opt_in | A customer has given the reminder single opt-in by agreeing in the chat. |
| reminder_single_opt_in_asked | A customer was asked in chat whether they agree to receive a reminder. |
| reminder_single_opt_in_rejected | A customer did not agree to receive a reminder in chat. |
| welcome_sent | A welcome message was sent in a welcome process module to a new customer. |
| welcome_sent_recurrent | A welcome message was sent in a welcome process module to a recurrent customer. |
| welcome_sent_recurrent_named | A welcome message was sent in a welcome process module to a signed-in customer with name. |
| win_lost | A customer has not won in a win process module. |
| win_participant_bpmn_process | A customer has participated for the first time in a process in a win process module. |
| win_participant_bpmn_sub_process | A customer has participated for the first time in a win process module. |
| win_participation | A customer has participated in a win process module. |
| win_won | A customer has won in a win process module. |

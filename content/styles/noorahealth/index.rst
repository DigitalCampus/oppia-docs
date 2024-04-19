NooraHealth Style
====================


Permissions
------------

For editing content in Moodle, you will need and account with teacher permissions - accounts and permissions for this
need to be requested from Digital Campus.

For publishing and updating courses to the Oppia server, you will need permissions for this (the Noora team have admin
accounts to enable these permissions), see: :doc:`/implementers/dashboard/users`


Terminology
------------

A 'module' for NooraHealth is equivalent to a 'course' in Moodle.
A 'lesson' for NooraHealth is equivalent to a 'topic' in Moodle.

Applying the styles
-----------------------

For this style, the page content in Moodle needs to be edited/updated when using the HTML code view, these styles can't
be applied only using the WYSIWYG editor view.

To access the HTML code view, first click on the editor icon in the top left:

.. image:: images/moodle-html1.png
    :width: 400 px

Then click on the code view icon in the bottom right:

.. image:: images/moodle-html2.png
    :width: 400 px


Intro Section
~~~~~~~~~~~~~~

Example:: 

    <intro-section>
        <img src="image.jpg" alt="" role="presentation" class="img-fluid atto_image_button_text-bottom">
        <content>
            <module-title>MODULE 1:</module-title>
            <module-description>Getting started with the Care Companion Program</module-description>
            <lesson-title>LESSON 1:</lesson-title>
            <lesson-description>Setting Context</lesson-description>
        </content>
    </intro-section>



Example output:

.. image:: images/intro-section.png
    :width: 200 px


Video Section
~~~~~~~~~~~~~~

Example::

    <video-section>
        <video poster="video.png" controls="true">
            <source src="video.mp4">video.mp4
        </video>
    </video-section>

.. note::
   *video.png* must be replaced by the full path of the thumbnail image.

   *video.mp4* must be replaced by the full path of the video file.

Example output:

.. image:: images/video-section.png
    :width: 200 px


Audio Section
~~~~~~~~~~~~~~

Example::

    <audio-section>
        <content>
            <p><strong>Play the audio to hear Roopa’s story.</strong></p>

            <!-- The next line is optional, only when you want to add an image above the audio player -->
            <img src="audio.png" alt="" width="200" height="200" role="presentation" class="img-fluid atto_image_button_text-bottom">

            <audio controls="true">
                <source src="audio.mp3">audio.mp3
            </audio>
        </content>
    </audio-section>

.. note::
   *audio.png* must be replaced by the full path of the image that will display above the audio player.

   *audio.mp3* must be replaced by the full path of the audio file.

Example output:

.. image:: images/audio-section.png
    :width: 200 px
    
    
Noor Section
~~~~~~~~~~~~~~

Example::

    <noor-section>
        <slide>
            <noor icon="1"></noor>
            <p>Hello, my name is <strong><em>‘Noor’</em></strong>. I am excited to be here with you today.</p>
        </slide>
        <slide>
            <noor icon="1"></noor>
            <p>I am your online assistant, and I will guide you through this program</p>
        </slide>
        <slide>
            <noor icon="2"></noor>
            <p>Through these modules, I will take you through a step by step process of becoming a CCP Trainer.</p>
        </slide>
    </noor-section>

Example output:

.. image:: images/noor-section-1.png
    :width: 200 px  
    
.. image:: images/noor-section-3.png
    :width: 200 px 
    
Content Section
~~~~~~~~~~~~~~~~

Example::

    <content-section pagination="true">
        <slide>
            <img src="nurse_bhakti_1.png" alt="Nurse Bhakti" width="200" height="215" class="img-fluid atto_image_button_text-bottom">
            <p>Nurse Bhakti has been working in the neo-natal ward at SNR District Hospital, Kolar for more than a decade. As a senior nurse, she has many responsibilities— meeting patients, talking to their families, administering medicine, doing rounds with the doctor and maintaining the records.</p>
        </slide>
        <slide>
            <img src="nurse_bhakti_2.png" alt="" width="200" height="170" role="presentation" class="img-fluid atto_image_button_text-bottom">
            <p>One day during her rounds, she met a one-week old baby who had been admitted to the ward. The baby was constantly crying.</p>
            <p>When nurse Bhakti asked the mother what the problem was, she was told that the mother had been facing difficulties in breastfeeding the baby since a couple
                of days.</p>
        </slide>
        <slide>
            <img src="nurse_bhakti_3.png" alt="Nurse Bhakti kept checking if the mother was following her instructions." width="200" height="99" role="presentation" class="img-fluid atto_image_button_text-bottom">
            <p>An elderly neighbor had suggested the family to give the baby some baby food mixed with water. The worried parents had followed this advice, but the baby developed loose stools, refused to eat, and wouldn't stop crying.
                The family was concerned. They rushed to mother and baby to the district hospital.
            </p>
        </slide>
        <slide>
            <img src="nurse_bhakti_4.png" alt="" width="200" height="161" role="presentation" class="img-fluid atto_image_button_text-bottom">
            <p>The doctor immediately admitted the baby and asked the mother to exclusively breastfeed the child. But the mother was still experiencing pain while feeding the baby and did not know what to do.
                Nurse Bhakti noticed that the mother was scared. She told her not to worry and showed her the correct breastfeeding techniques.The frightened young mother and her family followed all of Nurse Bhakti’s instructions.
            </p>
        </slide>
        <slide>
            <img src="nurse_bhakti_5.png" alt="" width="200" height="170" role="presentation" class="img-fluid atto_image_button_text-bottom">
            <p>Over the next few days, Nurse Bhakti kept checking if the mother was following her instructions. She also made sure that the mother was eating nutritious and well-balanced meals. With the mother following the right breastfeeding techniques, the baby’s health improved. </p>
    
            <p>The mother and the family were grateful to Bhakti for her efforts.</p>
        </slide>  
    </content-section>

Example output:

.. image:: images/content-section-1.png
    :width: 200 px  
    
.. image:: images/content-section-2.png
    :width: 200 px 


Feedback Section
~~~~~~~~~~~~~~~~

Example::

    <info-section type="feedback">
        <content>
            <p>Over the last couple of months, I have spoken to a few nurses from different parts of the world</p>
            <p><strong>Here is what they said:</strong></p>
            <noora-button color="green"><em>“I spend a lot of time talking to patients and their families about how to care take of themselves better.”</em></noora-button><br>
            <noora-button color="green"><em>“I feel patients and their families respect me because of my uniform and my knowledge.”</em></noora-button><br>
            <noora-button color="green"><em>“Apart from taking care of patients many times I also provide emotional support to patients and their families”</em>.<br></noora-button><br>
            <p><strong>Tap on the statement which you agree with the most</strong></p>
    
        </content>
    </info-section>

Example output:

.. image:: images/feedback.png
    :width: 200 px 

Info Section
~~~~~~~~~~~~~~~~

Example::

    <info-section>
        <slide>
            <img src="content-image-6.png" alt="" width="150" height="150" role="presentation" class="img-fluid atto_image_button_text-top">
            <p>Nurse Bhakti's story is not unique.</p>
            <p>As a nurse, you are the <span color="pink">main person of contact</span> for patients and families. You go above and beyond your duty for many patients.</p>
        </slide>
        <slide>
            <img src="content-image-6.png" alt="" width="150" height="150" role="presentation" class="img-fluid atto_image_button_text-top">
            <p>With CCP, the <span color="pink">responsibility of patient care</span> is shared between doctors, nurses, and families/caregivers.</p>
        </slide>
        <slide>
            <img src="content-image-7.png" alt="" width="166" height="167" role="presentation"  class="img-fluid atto_image_button_text-top">
            <p>Noora Health has trained over 12,00,000 nurses in different parts of the country.</p>
    
            <p><span color="pink">The Care Companion Program has impacted nearly 57,00,000 families</span> to be able to take care of their health. </p>
        </slide>
        <slide>
            <img src="content-image-8.png" alt="" width="136" height="136" role="presentation" class="img-fluid atto_image_button_text-top">
            <p>As a CCP Trainer, you will also join this journey and create a difference in the lives of many patients and their families.</p>
    
            <p color="pink">You are not alone in this journey</p>
            <p><strong>Noora Health is here to support you throughout.</strong></p>
        </slide>
    </info-section>


Example output:

.. image:: images/info-section-1.png
    :width: 200 px  
    
.. image:: images/info-section-2.png
    :width: 200 px

.. note::
   Using ``<info-section type="specify-the-type-here">`` you can get different background variations of the info section. The allowed values are: 1, 2, 3, 4, gallery, and feedback. And the result are the following:

   +-----------------------------------------+-----------------------------------------+-----------------------------------------+
   | .. figure:: images/info-section-1.png   | .. figure:: images/info-section-3.png   | .. figure:: images/info-section-4.png   |
   |   :width: 100%                          |   :width: 100%                          |   :width: 100%                          |
   |                                         |                                         |                                         |
   |   type="1"                              |   type="2"                              |   type="3"                              |
   +-----------------------------------------+-----------------------------------------+-----------------------------------------+
   | .. figure:: images/info-section-5.png   | .. figure:: images/info-section-6.png   | .. figure:: images/info-section-7.png   |
   |   :width: 100%                          |   :width: 100%                          |   :width: 100%                          |
   |                                         |                                         |                                         |
   |   type="4"                              |   type="gallery"                        |   type="feedback"                       |
   +-----------------------------------------+-----------------------------------------+-----------------------------------------+



What we learned Section
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Example::

    <what-we-learned-section>
        <section-title>What we learned in this lesson</section-title>
    
        <card left="" color="orange">
            <content>
                <img src="M1L1_what_we_learned_1.png" alt="" width="200" height="200" role="presentation" class="img-fluid atto_image_button_text-bottom">
                <p>As nurses, you spend a significant amount of time with patients, who look up to you for advice and guidance.</p>
            </content>
        </card>
    
        <card right="" color="pink">
            <content>
                <img src="M1L1_what_we_learned_2.png" alt="" width="200" height="200" role="presentation" class="img-fluid atto_image_button_text-bottom">
                <p>By sharing accurate medical information with patients and their families, you engage them, transforming the patient's health into a shared responsibility.
                </p>
            </content>
        </card>
    </what-we-learned-section>


Example output:

.. image:: images/what-we-learned-section-1.png
    :width: 200 px  
    
.. image:: images/what-we-learned-section-2.png
    :width: 200 px 

Next Lesson Section
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Example::

    <next-lesson-section>
        <img src="sample_image.png" width="200" height="200" role="presentation" class="img-fluid atto_image_button_text-bottom">
        In the next lesson we will talk about how the <strong>Care Companion program</strong> plays a role in shared caregiving.
    </next-lesson-section>

Example output:

.. image:: images/next-lesson-section.png
    :width: 200 px  
    
 
Index Section
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Example::

    <index-section>
        <content>
            <p>When we talk of the care companion model, it has three parts to it:</p>
            <item order="1">
                The Care Companion Program sessions.
            </item>
            <item order="2">
                Mobile Care Companion Service (MCCS)
            </item>
            <item order="3">
                Implementation Support
            </item>
        </content>
    </index-section>

Example output:

.. image:: images/index-section.png
    :width: 200 px 


Chapter Section
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Example::

    <chapter-section>
        <content>
            <p>Chapter 1:<br><strong>The Care Companion Program (CCP) sessions</strong></p>
            <img src="M1L1_what_we_learned_1.png" alt="" width="200" height="200" role="presentation" class="img-fluid atto_image_button_text-bottom">
        </content>
    </chapter-section>

Example output:

.. image:: images/chapter-section.png
    :width: 200 px 

Know Mode Slides
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Example::

    <info-section>
        <slide>
            <p class="lead">Let us quickly see some of the <strong><span color="pink">impact</span></strong> in different health conditions.</p>
        </slide>
        <slide>
            <p class="lead">
                <br><br><br><br>Click on each disease area to know about the impact in each of the conditions.
            </p>
            <small>Click the highlighted button to know more.</small>
            <know-more color="pink">
                <item highlighted="">
                    <span>Cardiac Health</span>
                    <modal>
                        <card-content>
                            For Cardiac Patients, 71% reduction in 30 day post surgical complications.
                        </card-content>
                    </modal>
                </item>
                <item>
                    <span> Maternal and Child Health</span>
                    <modal>
                        <card-content>
                            For Maternal and newborns, 56% Reduction in newborn readmissions and 18% reduction in newborn mortality.
                        </card-content>
                    </modal>
                </item>
                <item>
                    <span>During Covid</span>
                    <modal>
                        <card-content>
                            During Covid 19, 48% reduction in hospitalization
                        </card-content>
                    </modal>
                </item>
            </know-more>
        </slide>
    </info-section>

.. note::
   You can change the color using ``<know-more color="pink">`` and the color of your choice between: pink, blue, orange or green.

   If no color is specified, pink will be used.

Example output:

.. image:: images/know-more-1.png
    :width: 200 px 

.. image:: images/know-more-2.png
    :width: 200 px
    
.. image:: images/know-more-3.png
    :width: 200 px 


Content Image Grid
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Example::

    <content-section color="black">
        <content>
            <p class="lead"><strong>Think of places where -</strong></p>
            <div class="columns">
                <div>
                    <img src="m1l3-trainer1.png" alt="CCP Trainers" width="300" height="300" class="img-fluid atto_image_button_text-bottom">
                    A group of patients can sit.
                </div>
                <div>
                    <img src="CCP%20Places.png" alt="CCP Places" width="300" height="300" class="img-fluid atto_image_button_text-bottom">
                    You can easily
                    display the CCP tools
                </div>
            </div>
            <div class="columns">
                <div>
                    <img src="hccp-places3.png" alt="CCP Places" width="300" height="300" class="img-fluid atto_image_button_text-bottom">
                    You can display the posters provided for CCP sessions.
                </div>
                <div>
                    <img src="m1l3-role5.png" alt="CCP Places" width="300" height="300" class="img-fluid atto_image_button_text-bottom">
                    Gathering patients and family members is convenient
                </div>
            </div>
        </content>
    </content-section>

Example output:

.. image:: images/image-grid.png
    :width: 200 px 


Content Card
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Example::

    <info-section>
        <content>
            <know-more class="columns">
                <div>
                    <item highlighted="">
                        <img src="ic-master-trainer.png" alt="trainer" width="256" height="378" class="img-fluid atto_image_button_text-bottom">
                        <modal color="blue">
                            <card-content>
                                <img src="m1l3-master0.png" alt="" width="137" height="177" role="presentation" class="img-fluid atto_image_button_middle">
                                <h1>Who is a Master Trainer?</h1>
                                A master trainer is a nurse nominated by the facility.
                                The selected nurse attends the in-person training conducted by the Noora Health training team.
                                The master trainer learns about conducting a CCP session and how to support the other nurses in the hospital to conduct these sessions.
                            </card-content>
                        </modal>
                    </item>
                    Master Trainer
                </div>
                <div>
                    <item>
                        <img src="ic-trainer.png" alt="Trainer" width="256" height="378" class="img-fluid atto_image_button_text-bottom">
                        <modal color="blue">
                            <card-content>
                                <img src="m1l3-trainer0.png" alt="" width="137" height="177" role="presentation" class="img-fluid atto_image_button_middle">
                                <h1>Who is a CCP Trainer?</h1>
                                All the nurses, such as you, in the facility attend the online training module and learns how to conduct CCP sessions.
                                After completing the training, you qualify as a CCP trainers.
                            </card-content>
                        </modal>
                    </item>
                    Trainer
                </div>
            </know-more>
            <p><span class="lead">Click on each role to know more about them and their roles and responsabilities.</span><small><br>
                    Click the highlighted button to know more.</small></p>
        </content>
    </info-section>


Example output:

.. image:: images/content-card-1.png
    :width: 200 px 
    
.. image:: images/content-card-2.png
    :width: 200 px 
    
Quizzes and Feedback
----------------------

The overall style for quizzes is defined directly in the app, so can't be changed within Moodle.

For the feedback responses, you have to add the following styles under the "Feedback" field under each Moodle answer (using the HTML code view):

For correct response::

    <feedback-result>
        <feedback-card color="green">
            <content>
                <h1 color="green">Success!</h1>
                <answer>"Giving medical information to patients and families"</answer>
                <p>The purpose of a CCP session is to provide accurate medical information and skills to take care of the patient.</p>
                <p>During the CCP session you will not just be sharing information but also interacting with participants to ensure that they understand what you are saying.</p>
                <p>The patients will be able to use the information when they go home.</p>
            </content>
        </feedback-card>
    </feedback-result>
    
Example output:

.. image:: images/quiz-feedback-correct.png
    :width: 200 px 
    
For incorrect response::

    <feedback-result>
        <feedback-card color="pink">
            <content>
                <h1 color="pink">Oh no!</h1>
                <p color="pink">The correct answer is:</p>
                <answer>
                    <table style="text-align: center;">
                        <tbody>
                            <tr>
                                <td style="text-align: center;"><img src="patient-family.png" alt="" width="111" height="120" role="presentation"></td>
                                <td style="text-align: center;"><img src="nurse.png" alt="" width="111" height="120" role="presentation"></td>
                                <td style="text-align: center;"><img src="visual-aids.png" alt="" width="111" height="120" role="presentation"></td>
                            </tr>
                            <tr>
                                <td style="text-align: center;">Patients &amp; family members</td>
                                <td style="text-align: center;">Nurse</td>
                                <td style="text-align: center;">Visual Aids like Flipcharts</td>
                            </tr>
                        </tbody>
                    </table>
                </answer>
                <p>A CCP session is conducted by the nurse using visual aids such as flipcharts, models, charts, etc.</p>
                <p>These visual aids are used to help people relate to the material being taught,<strong> promoting better understanding, and improving retention.</strong></p>
            </content>
        </feedback-card>
    
Example output:

.. image:: images/quiz-feedback-incorrect.png
    :width: 200 px 

For multiple choice questions, where there is only one correct answer, enter the feedback into the feedback field
corresponding to the response option.


For multiple select questions, where there is more than one correct answer, enter the feedback in the 'combined
feedback' section, either the "For any correct response" or "For any incorrect response" fields. The correct response
feedback is given to the user if they get the question 100% correct, otherwise they will get the incorrect response
feedback.

Activity Time Section
~~~~~~~~~~~~~~~~

Example::

    <activity-time-section>
        <content>
            <img src="activity_time.png" alt="" width="200" height="180" role="presentation" class="img-fluid atto_image_button_text-bottom">

            <h1>Activity Time</h1>
            <p>Use your knowledge about conducting CCP sessions to find a spot in your department for the session.</p>
        </content>
    </activity-time-section>

.. note::
   Replace *activity_time.png* with the full path of the desired image.

Example output:

.. image:: images/activity-time-section.png
    :width: 200 px
